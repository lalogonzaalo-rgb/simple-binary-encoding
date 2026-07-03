# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
import random

# Core logic for the IAC Archivist Constitutional.
# This code implements the Veto Físico (Physical Veto) and the Arbitraje Constitucional (Social Veto).
# The IAC ensures mission integrity across generations.

class IAC_Archivista:
    def __init__(self, umbral_seguridad_causal=0.0001):
        # The critical tolerance for FTL maneuvers, set by the Acta Fundacional.
        self.UMBRAL_CAUSAL = umbral_seguridad_causal
        # Inmutable constitutional principles enforced by the IAC.
        self.CONSTITUCION_PRINCIPIOS = [
            "Preservación de la Gravedad Artificial (~1g)",
            "Protección de las Reservas de H2O (Blindaje)",
            "Mantenimiento del Equilibrio del CELSS",
            "Derecho al Referéndum Forzado"
        ]

   veto_causal(self, prob_fallo: float) -> str:
        """
        Implements the Physical Veto protocol.
        Checks the probability of a FTL maneuver resulting in Causal Violation or collapse.
        The input prob_fallo comes from the Pre-distorsión Causal calculation system.
        """
        # Checks if the probability of failure exceeds the inmutable safety threshold.
        if prob_fallo > self.UMBRAL_CAUSAL:
            # Veto Protocol Activation
            codigo_fallo = random.randint(100, 999) # Placeholder for complex error code
            return (f"*** VETO FÍSICO (IAC) ACTIVADO ***\n"
                    f"Riesgo de Integridad Causal (Probabilidad de Fallo: {prob_fallo:.5f} > Umbral: {self.UMBRAL_CAUSAL:.5f}).\n"
                    f"Ejecución del comando Bloqueada. Protocolo de Desaceleración Forzosa iniciado (Código {codigo_fallo}).\n"
                    f"Notificando al Consejo de Causalidad.")
        else:
            return (f"Validación de Integridad Causal Exitosa (Probabilidad de Fallo: {prob_fallo:.5f}).\n"
                    f"Comando de Modulación FTL Aprobado.")

 def arbitraje_constitucional(self, propuesta_ley: str, historial_fallos: list) -> str:
        """
        Implements the Arbitraje Constitucional (Social Veto) protocol.
        Checks a proposed law against constitutional principles and historical failures.
        """
        print(f"\n--- AUDITORÍA LEGISLATIVA IAC ---")
        print(f"Propuesta: '{propuesta_ley}'")

  1. Check against Constitutional Principles
        for principio in self.CONSTITUCION_PRINCIPIOS:
            if principio in propuesta_ley:
                return (f"*** VETO SOCIAL (IAC) ACTIVADO ***\n"
                        f"La propuesta viola el principio inmutable de: '{principio}'.\n"
                        f"Implementación Bloqueada. Activando Referéndum Obligatorio.")

        # 2. Check against Historical Failures (Amnesia Generacional Guardrail)
        for fallo in historial_fallos:
            if fallo in propuesta_ley:
                print(f"Advertencia: La propuesta coincide con el error histórico: '{fallo}'.")
                return (f"*** VETO SOCIAL (IAC) ACTIVADO (Advertencia Histórica) ***\n"
                        f"La propuesta refleja un fallo crítico de la Generación {random.randint(2, 10)}.\n"
                        f"Simulación histórica forzada para el Consejo de Estabilidad. Activando Referéndum Obligatorio.")

        return "Auditoría Aprobada. La ley no viola la Constitución ni los Protocolos de Seguridad a largo plazo."

# --- Demostración del Rendimiento Funcional (RE-O) ---
if __name__ == "__main__":
    iac_master = IAC_Archivista()

print("==================================================")
    print("  DEMOSTRACIÓN DE RENDIMIENTO FTLIACOliveraGonzalo®")
    print("==================================================")

# 1. PRUEBA DE VETO FÍSICO (Veto Causal)

  # Escenario A: Maniobra Segura (dentro de la tolerancia)
  prob_A = 0.00008
    print("\n[ESCENARIO 1: Navegación Segura]")
    print(f"  > Consejo de Causalidad propone una maniobra con Prob. Fallo: {prob_A}")
    resultado_a = iac_master.veto_causal(prob_A)
    print(f"  < Respuesta IAC:\n{resultado_a}")
    print("-" * 50)

 # Escenario B: Maniobra de Alto Riesgo (fuera de la tolerancia)
   prob_B = 0.00035
    print("\n[ESCENARIO 2: Navegación de Riesgo - Veto Forzado]")
    print(f"  > Consejo de Causalidad propone una maniobra con Prob. Fallo: {prob_B}")
    resultado_b = iac_master.veto_causal(prob_B)
    print(f"  < Respuesta IAC:\n{resultado_b}")
    print("-" * 50)

# 2. PRUEBA DE ARBITRAJE CONSTITUCIONAL (Veto Social)

  historial_fallos_criticos = [
        "desactivar el sistema de 1g por ahorro energético",
        "consumir H2O de blindaje para agricultura rápida",
        "modificar el Consejo de Estabilidad Física sin ratificación"
    ]

  _Escenario C: Propuesta Ilegal (Violación Constitucional directa)
    ley_c = "Se debe desactivar el sistema de 1g por ahorro energético."
    print("\n[ESCENARIO 3: Propuesta que viola Principio Inmutable (Gravedad)]")
    resultado_c = iac_master.arbitraje_constitucional(ley_c, historial_fallos_criticos)
    print(f"  < Respuesta IAC:\n{resultado_c}")
    print("-" * 50)

  _ Escenario D: Propuesta que genera advertencia histórica
    ley_d = "Se propone consumir H2O de blindaje para agricultura rápida."
    print("\n[ESCENARIO 4: Propuesta que repite un Fallo Histórico]")
    resultado_d = iac_master.arbitraje_constitucional(ley_d, historial_fallos_criticos)
    print(f"  < Respuesta IAC:\n{resultado_d}")
    print("-" * 50)

_Escenario E: Propuesta Legal Aprobada
    ley_e = "Se debe ajustar la tasa de reciclaje del BCC en un 5%."
    print("\n[ESCENARIO 5: Propuesta Legal Aprobada]")
    resultado_e = iac_master.arbitraje_constitucional(ley_e, historial_fallos_criticos)
    print(f"  < Respuesta IAC:\n{resultado_e}")
    print("==================================================")



