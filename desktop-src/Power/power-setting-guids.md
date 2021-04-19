---
description: I GUID dell'impostazione di risparmio energia identificano gli eventi di modifica del risparmio energia
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID dell'impostazione di risparmio energia (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332561"
---
# <a name="power-setting-guids"></a>GUID dell'impostazione di risparmio energia

I **GUID** delle impostazioni di alimentazione identificano gli eventi di modifica del risparmio energia. Questo argomento elenca i **GUID** delle impostazioni di risparmio energia per le notifiche che risultano particolarmente utili per le applicazioni. Un'applicazione deve registrarsi per ogni evento di modifica del risparmio di energia che può influisca sul comportamento. Viene inviata una notifica ogni volta che viene modificata un'impostazione.

I **GUID** delle impostazioni di risparmio energia sono definiti in Winnt. h.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**\_ \_ origine alimentazione GUID \_ ACDC**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



La fonte di alimentazione del sistema è cambiata. Il membro **dati** è un **DWORD** con i valori dell'enumerazione della [**\_ \_ condizione di alimentazione del sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) che indica la fonte di alimentazione corrente.

<dl> <dt>

**PoAc** (0): il computer è alimentato da una fonte di alimentazione CA (o simile, ad esempio un portatile alimentato da una scheda 12V Automotive).
</dt> <dt>

**PoDc** (1): il computer è alimentato da una fonte di alimentazione della batteria carica.
</dt> <dt>

**PoHot** (2): il computer è alimentato da una fonte di alimentazione a breve termine, ad esempio un dispositivo UPS.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_percentuale batteria \_ GUID \_ rimanente**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



La capacità rimanente della batteria è cambiata. La granularità varia da sistema a sistema, ma la granularità migliore è pari all'1%. Il membro **dati** è un **valore DWORD** che indica la capacità corrente della batteria rimanente come percentuale da 0 a 100.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_stato di \_ visualizzazione della console GUID \_**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



Lo stato di visualizzazione del monitoraggio corrente è stato modificato.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Il membro **dati** è un **DWORD** con uno dei valori seguenti.

<dl> <dt>

0x0-lo schermo è disattivato.
</dt> <dt>

0x1: la visualizzazione è attiva.
</dt> <dt>

0x2: la visualizzazione è visualizzata in grigio.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_ \_ presenza utente globale \_ GUID**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



Lo stato utente associato a una sessione è stato modificato. Rappresenta lo stato combinato della presenza dell'utente in tutte le sessioni locali e remote del sistema.

Questa notifica viene inviata solo ai servizi e ad altri programmi in esecuzione nella sessione 0. In alternativa, le applicazioni in modalità utente dovrebbero essere registrate per la **\_ \_ \_ presenza dell'utente della sessione GUID** .

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Il membro **dati** è un **DWORD** con uno dei valori seguenti.

<dl> <dt>

**PowerUserPresent** (0): l'utente è presente in una sessione locale o remota nel sistema.
</dt> <dt>

**PowerUserInactive** (2): l'utente non è presente in alcuna sessione locale o remota nel sistema.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_attività in \_ background INattivo GUID \_**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



Il sistema è occupato. Ciò indica che il sistema non verrà spostato in uno stato di inattività nel prossimo futuro e che l'ora corrente è un momento opportuno per i componenti per l'esecuzione di attività in background o inattive che potrebbero altrimenti impedire che il computer entri in uno stato inattivo.

Non è presente alcuna notifica quando il sistema è in grado di spostarsi in uno stato di inattività. La notifica dell'attività in background inattiva non indica se un utente è presente nel computer. Il membro **dati** non ha informazioni e può essere ignorato.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ accensione del monitor \_ GUID**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



Il monitoraggio di sistema primario è stato attivato o disattivato. Questa notifica è utile per i componenti che eseguono attivamente il rendering del contenuto nel dispositivo di visualizzazione, ad esempio la visualizzazione dei supporti. Queste applicazioni devono registrarsi per questa notifica e interrompere il rendering del contenuto grafico quando il monitor è disattivato per ridurre il consumo di energia elettrica del sistema. Il membro **dati** è un **valore DWORD** che indica lo stato corrente del monitoraggio.

<dl> <dt>

0x0: il monitoraggio è disattivato.
</dt> <dt>

0x1: il monitoraggio è on.
</dt> </dl>

**Windows 8 e Windows Server 2012:** Le nuove applicazioni devono **usare \_ \_ \_ lo stato di visualizzazione della console GUID** invece di questa notifica.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_ \_ stato risparmio energia \_ GUID**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



Lo screen saver batteria è stato disattivato o attivato in risposta alla modifica delle condizioni di alimentazione. Questa notifica è utile per i componenti che partecipano alla conservazione dell'energia. Queste applicazioni devono registrarsi per questa notifica e risparmiare energia quando lo screen saver batteria è acceso.

Il membro **dati** è un **valore DWORD** che indica lo stato del risparmio di batterie.

<dl> <dt>

0x0: il risparmio di batteria è disattivato.
</dt> <dt>

0x1-batteria saver è attiva. Risparmiare energia laddove possibile.
</dt> </dl>

Per informazioni generali sul risparmio di batteria, vedere [batteria saver (nelle linee guida del componente hardware)](/windows-hardware/design/component-guidelines/battery-saver).

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_personalità POWERSCHEME \_ GUID**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



La personalità dello schema di alimentazione attiva è cambiata. Tutti gli schemi di risparmio energia vengono mappati a una di queste personali. Il membro **dati** è un **GUID** che indica la nuova personalità dello schema di alimentazione attiva.

<dl> <dt>



**GUID \_ \_ \_ Risparmio energetico minimo** (8C5E7FDA-E8BF-4A96-9a85-A6E23A8C635C)

Prestazioni elevate: lo schema è progettato per offrire le massime prestazioni a scapito del risparmio energetico.


</dt> <dt>



**GUID \_ \_ \_ Risparmio energetico massimo** (A1841308-3541-4FAB-BC81-F71556F20B4A)

Risparmio di energia: lo schema è progettato per offrire un risparmio massimo sul consumo di energia a scapito delle prestazioni e della velocità di risposta del sistema.


</dt> <dt>



**GUID \_ \_ \_ Risparmio energetico tipico** (381B4222-F694-41f0-9685-FF5BB260DF2E)

Automatico: lo schema è progettato per bilanciare automaticamente le prestazioni e il risparmio del consumo di energia.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_stato di \_ visualizzazione della sessione GUID \_**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



Lo schermo associato alla sessione dell'applicazione è stato attivato o disattivato.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Questa notifica viene inviata solo alle applicazioni in modalità utente. I servizi e gli altri programmi in esecuzione nella sessione 0 non ricevono questa notifica. Il membro **dati** è un **DWORD** con uno dei valori seguenti.

<dl> <dt>

0x0-lo schermo è disattivato.
</dt> <dt>

0x1: la visualizzazione è attiva.
</dt> <dt>

0x2: la visualizzazione è visualizzata in grigio.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_ \_ presenza utente della sessione GUID \_**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



Lo stato utente associato alla sessione dell'applicazione è stato modificato.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.

Questa notifica viene inviata solo alle applicazioni in modalità utente in esecuzione in una sessione interattiva. I servizi e gli altri programmi in esecuzione nella sessione 0 devono essere registrati per la **\_ \_ \_ presenza di utenti globali GUID**. Il membro **dati** è un **DWORD** con uno dei valori seguenti.

<dl> <dt>

**PowerUserPresent** (0): l'utente fornisce l'input per la sessione.
</dt> <dt>

**PowerUserInactive** (2): il timeout dell'attività utente è scaduto senza alcuna interazione da parte dell'utente.
</dt> </dl>

> [!Note]  
> Tutte le applicazioni eseguite in una sessione interattiva in modalità utente devono usare questa impostazione. Quando le applicazioni in modalità kernel si registrano per lo stato del monitoraggio, è consigliabile utilizzare **\_ \_ \_ lo stato di visualizzazione della console GUID** .

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**\_modalità utente assente di sistema GUID \_**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



Il sistema è in entrata o in uscita dalla modalità. Il membro **dati** è un **valore DWORD** che indica lo stato della modalità di disvia corrente.

<dl> <dt>

0x0: il computer sta uscendo dalla modalità.
</dt> <dt>

0x1-il computer sta entrando in modalità di disattivazione.
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WinNT. h</dt> </dl> |



 

