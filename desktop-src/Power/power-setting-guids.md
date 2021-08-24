---
description: I GUID delle impostazioni di risparmio energia identificano gli eventi di risparmio energia.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID delle impostazioni di risparmio energia (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b05909509e0c3ed581582ebe90b10e5df4e91a31b7ab050b3fd1ef6679b1a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887031"
---
# <a name="power-setting-guids"></a>GUID delle impostazioni di risparmio energia

I **GUID** delle impostazioni di risparmio energia identificano gli eventi di modifica dell'alimentazione. Questo argomento elenca i GUID delle impostazioni **di** risparmio energia per le notifiche più utili per le applicazioni. Un'applicazione deve registrarsi per ogni evento di modifica dell'alimentazione che potrebbe influire sul relativo comportamento. La notifica viene inviata ogni volta che un'impostazione cambia.

I **GUID delle impostazioni** di risparmio energia sono definiti in WinNT.h.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID \_ ACDC \_ POWER \_ SOURCE**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



L'origine di alimentazione del sistema è stata modificata. Il **membro Dati** è un valore **DWORD** con valori dell'enumerazione [**SYSTEM POWER \_ \_ CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) che indica l'origine di alimentazione corrente.

<dl> <dt>

**PoAc** (0) - Il computer è alimentato da una fonte di alimentazione CA (o simile, ad esempio un computer portatile alimentato da un adattatore automobilistico da 12 V).
</dt> <dt>

**PoDc** (1): il computer è alimentato da una fonte di alimentazione a batteria di onboard.
</dt> <dt>

**PoHot** (2): il computer è alimentato da una fonte di alimentazione a breve termine, ad esempio un dispositivo UPS.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**PERCENTUALE \_ DI BATTERIA GUID \_ \_ RIMANENTE**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



La capacità rimanente della batteria è stata modificata. La granularità varia da sistema a sistema, ma la granularità più fine è dell'1%. Il **membro** dati è **un valore DWORD** che indica la capacità corrente della batteria rimanente come percentuale da 0 a 100.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**STATO \_ DI VISUALIZZAZIONE DELLA CONSOLE \_ \_ GUID**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



Lo stato di visualizzazione del monitoraggio corrente è stato modificato.

**Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Il **membro** Dati è **un valore DWORD** con uno dei valori seguenti.

<dl> <dt>

0x0: lo schermo è disattivato.
</dt> <dt>

0x1: lo schermo è on.
</dt> <dt>

0x2: lo schermo è in grigio.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**PRESENZA \_ UTENTE \_ GLOBALE \_ GUID**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



Lo stato utente associato a qualsiasi sessione è stato modificato. Rappresenta lo stato combinato della presenza dell'utente in tutte le sessioni locali e remote del sistema.

Questa notifica viene inviata solo ai servizi e ad altri programmi in esecuzione nella sessione 0. Le applicazioni in modalità utente devono invece registrarsi **per IL GUID SESSION USER \_ \_ \_ PRESENCE.**

**Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Il **membro** Dati è **un valore DWORD** con uno dei valori seguenti.

<dl> <dt>

**PowerUserPresent** (0): l'utente è presente in qualsiasi sessione locale o remota nel sistema.
</dt> <dt>

**PowerUserInactive** (2): l'utente non è presente in alcuna sessione locale o remota nel sistema.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**ATTIVITÀ IN \_ \_ BACKGROUND INATTIVA GUID \_**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



Il sistema è occupato. Ciò indica che il sistema non verrà inattivo nel prossimo futuro e che il tempo corrente è un buon momento per i componenti per eseguire attività in background o inattive che altrimenti impedirebbe al computer di entrare in uno stato di inattività.

Non viene visualizzata alcuna notifica quando il sistema è in grado di passare a uno stato di inattività. La notifica dell'attività in background inattiva non indica se un utente è presente nel computer. Il **membro** dati non dispone di informazioni e può essere ignorato.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID \_ MONITOR \_ POWER \_ ON**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



Il monitor di sistema primario è stato acceso o spento. Questa notifica è utile per i componenti che eseguono attivamente il rendering del contenuto nel dispositivo di visualizzazione, ad esempio la visualizzazione dei supporti. Queste applicazioni devono registrarsi per questa notifica e arrestare il rendering del contenuto grafico quando il monitoraggio è spento per ridurre il consumo di energia del sistema. Il **membro** Dati è un **valore DWORD** che indica lo stato corrente del monitoraggio.

<dl> <dt>

0x0: il monitoraggio è disattivato.
</dt> <dt>

0x1: il monitoraggio è on.
</dt> </dl>

**Windows 8 e Windows Server 2012:** Le nuove applicazioni devono usare **GUID \_ CONSOLE DISPLAY \_ \_ STATE** anziché questa notifica.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**STATO \_ DI RISPARMIO ENERGIA \_ \_ GUID**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



Il risparmio batteria è stato spento o acceso in risposta alla modifica delle condizioni di alimentazione. Questa notifica è utile per i componenti che partecipano alla conservazione dell'energia. Queste applicazioni devono registrarsi per questa notifica e risparmiare energia quando risparmio batteria è on.

Il **membro** Dati è un **valore DWORD** che indica risparmio batteria stato.

<dl> <dt>

0x0: il risparmio batteria è spento.
</dt> <dt>

0x1- Risparmio batteria è on. Risparmiare energia laddove possibile.
</dt> </dl>

Per informazioni generali sui risparmio batteria, vedere [risparmio batteria (nelle linee guida dei componenti hardware).](/windows-hardware/design/component-guidelines/battery-saver)

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**PERSONALITÀ \_ DI POWERSCHEME \_ GUID**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



La personalità della combinazione per il risparmio di energia attiva è cambiata. Tutte le combinazioni per il risparmio di energia vengono mappate a una di queste personalità. Il **membro dati** è un GUID **che** indica la nuova personalità della combinazione per il risparmio di energia attiva.

<dl> <dt>



**GUID \_ RISPARMIO \_ \_ ENERGETICO** MINIMO (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)

Prestazioni elevate: lo schema è progettato per offrire prestazioni massime a scapito del risparmio sul consumo di energia.


</dt> <dt>



**GUID \_ RISPARMIO \_ \_ MASSIMO** DI ENERGIA (A1841308-3541-4FAB-BC81-F71556F20B4A)

Risparmio di energia: lo schema è progettato per offrire un risparmio massimo sul consumo di energia a scapito delle prestazioni e della velocità di risposta del sistema.


</dt> <dt>



**GUID \_ RISPARMIO \_ \_ DI** ENERGIA TIPICO (381B4222-F694-41F0-9685-FF5BB260DF2E)

Automatico: lo schema è progettato per bilanciare automaticamente i risparmi sulle prestazioni e sul consumo di energia.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**STATO \_ DI VISUALIZZAZIONE DELLA SESSIONE \_ \_ GUID**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



La visualizzazione associata alla sessione dell'applicazione è stata attivata o disattivata.

**Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Questa notifica viene inviata solo alle applicazioni in modalità utente. I servizi e altri programmi in esecuzione nella sessione 0 non ricevono questa notifica. Il **membro** Dati è **un valore DWORD** con uno dei valori seguenti.

<dl> <dt>

0x0: lo schermo è disattivato.
</dt> <dt>

0x1: lo schermo è on.
</dt> <dt>

0x2: lo schermo è in grigio.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**PRESENZA \_ UTENTE \_ SESSIONE \_ GUID**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



Lo stato utente associato alla sessione dell'applicazione è stato modificato.

**Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Questa notifica viene inviata solo alle applicazioni in modalità utente in esecuzione in una sessione interattiva. I servizi e altri programmi in esecuzione nella sessione 0 devono registrarsi per **GUID \_ GLOBAL USER \_ \_ PRESENCE**. Il **membro** Dati è **un valore DWORD** con uno dei valori seguenti.

<dl> <dt>

**PowerUserPresent** (0): l'utente fornisce input alla sessione.
</dt> <dt>

**PowerUserInactive** (2): il timeout dell'attività utente è trascorso senza alcuna interazione da parte dell'utente.
</dt> </dl>

> [!Note]  
> Tutte le applicazioni eseguite in una sessione interattiva in modalità utente devono usare questa impostazione. Quando le applicazioni in modalità kernel si registrano per lo stato del monitoraggio, devono invece usare **\_ GUID CONSOLE DISPLAY \_ \_ STATUS.**

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID \_ SYSTEM \_ AWAYMODE**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



Il sistema sta uscendo dalla modalità di uscita. Il **membro** Dati è un **valore DWORD** che indica lo stato corrente della modalità non disponibile.

<dl> <dt>

0x0- Il computer sta uscendo dalla modalità.
</dt> <dt>

0x1: il computer sta per entrare in modalità di sospensione.
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WinNT.h</dt> </dl> |



 

