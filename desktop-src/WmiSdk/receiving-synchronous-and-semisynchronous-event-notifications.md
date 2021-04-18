---
description: Usare SWbemServices.ExecQuery per richiedere tutti gli eventi esistenti.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Ricezione di notifiche di eventi sincroni e semisincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314584"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Ricezione di notifiche di eventi sincroni e semisincrono

Usare [**SWbemServices.ExecQuery**](swbemservices-execquery.md) per richiedere tutti gli eventi esistenti.

Nell'esempio di codice seguente viene illustrato come eseguire una query per gli eventi in un log.

`Select * from Win32_NTLogEvent`

Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md), [ricezione di notifiche degli eventi](receiving-event-notifications.md)e [WQL (SQL per WMI)](wql-sql-for-wmi.md).

La chiamata predefinita a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usa la comunicazione semisincrono. Il parametro *iFlags* include i flag **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** impostati per impostazione predefinita. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Nella procedura seguente viene descritto come ricevere una notifica degli eventi semisincrono tramite VBScript.

**Per ricevere la notifica degli eventi semisincrono in VBScript**

1.  Creare una query per il tipo di evento che si desidera ricevere. Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).

2.  Se si richiede un tipo di istanza di un evento come [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indicare nella query un tipo di istanza di destinazione, ad esempio [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Se necessario, specificare un'istanza, ad esempio, il nome di uno spazio dei nomi quando si richiedono istanze [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) future per uno spazio dei nomi specifico.

4.  Specificare un intervallo di polling per Strumentazione gestione Windows (WMI) in una query, ad esempio "entro 10", per eseguire il polling ogni 10 secondi. Per ulteriori informazioni, vedere [clausola all'interno](within-clause.md)di.

5.  Chiamare [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utilizzando la query.

6.  Esegue il ciclo della raccolta ricevuta.

Nell'esempio seguente viene illustrato come monitorare l'inserimento e la rimozione di dischi da un'unità disco floppy in un computer locale. Lo script richiede \_ istanze di [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) per l'istanza [**di \_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dell'unità floppy ed esegue il polling ogni 10 secondi per le nuove istanze. Questo script è un esempio di consumer di eventi temporanei e continua l'esecuzione fino a quando non viene arrestato in Gestione attività o il sistema non viene riavviato. Per ulteriori informazioni, vedere [ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md).


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



Nella procedura seguente viene descritto come ricevere una notifica degli eventi semisincrono utilizzando C++.

**Per ricevere la notifica degli eventi semisincrono in C++**

1.  Configurare l'applicazione con le chiamate alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    Poiché WMI è basato su COM, chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) è un passaggio obbligatorio per un'applicazione WMI. Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).

2.  Determinare il tipo di eventi che si desidera ricevere.

    WMI supporta eventi intrinseci ed estrinseci. Un evento intrinseco è un evento predefinito da WMI. Un evento estrinseco è un evento definito da un provider di terze parti. Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).

3.  Eseguire la registrazione per ricevere una classe specifica di eventi con una chiamata al metodo [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .

    Eseguire ogni query in modo molto specifico. L'obiettivo della registrazione è registrarsi per ricevere solo le notifiche richieste. Notifiche che non sono necessarie per l'elaborazione e il tempo di recapito.

    È possibile progettare un consumer di eventi per la ricezione di più eventi. Ad esempio, un consumer potrebbe richiedere la notifica degli eventi di modifica dell'istanza per una classe specifica di eventi di violazione della sicurezza e del dispositivo. In questo caso, le attività eseguite da un consumer durante la ricezione di un evento di modifica dell'istanza sono diverse per i due eventi. Pertanto, il consumer deve effettuare una chiamata a [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) per registrare gli eventi di modifica dell'istanza e un'altra chiamata a **ExecNotificationQuery** per la registrazione degli eventi di violazione della sicurezza.

    Nella chiamata a [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)impostare il parametro *è* sul **\_ flag WBEM \_ return \_ immediatamente** e il **flag WBEM \_ \_ \_ solo in futuro**. Il **\_ flag WBEM \_ restituisce \_ immediatamente** un flag per l'elaborazione di semisincrono e il flag **WBEM di \_ \_ \_ sola trasmissione** richiede un enumeratore di solo inoltri. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md). La funzione **ExecNotificationQuery** restituisce un puntatore a un'interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

4.  Eseguire il polling per le notifiche degli eventi registrati eseguendo chiamate ripetute al metodo [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .
5.  Al termine, rilasciare l'enumeratore che fa riferimento all'oggetto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

    È possibile rilasciare il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) associato alla registrazione. Il rilascio del puntatore **IWbemServices** fa sì che WMI interrompa la distribuzione degli eventi a tutti i consumer temporanei associati.

 

 
