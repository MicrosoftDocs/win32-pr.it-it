---
description: Windows Strumentazione gestione (WMI) è l'infrastruttura per i dati di gestione e le operazioni Windows sistemi operativi basati su Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Strumentazione gestione Windows (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b08c0301881b57c8132be9eead2e5b52cb64d4d3c4278985a573d5bff94f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553135"
---
# <a name="windows-management-instrumentation"></a>Strumentazione gestione Windows (WMI)

## <a name="purpose"></a>Scopo

Windows Strumentazione gestione (WMI) è l'infrastruttura per i dati di gestione e le operazioni Windows sistemi operativi basati su Windows. È possibile scrivere script o applicazioni WMI per automatizzare le attività amministrative nei computer remoti, ma WMI fornisce anche dati di gestione ad altre parti del sistema operativo e dei prodotti, ad esempio System Center Operations Manager, in precedenza Microsoft Operations Manager (MOM) o gestione remota Windows[(WinRM).](/windows/desktop/WinRM/portal)

> [!Note]  
> La documentazione seguente è destinata agli sviluppatori e agli amministratori IT. Gli utenti finali che hanno riscontrato un messaggio di errore relativo a WMI devono passare a [Supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore. Per altre informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI è completamente supportato da Microsoft. Tuttavia, la versione più recente di scripting amministrativo e controllo è disponibile tramite Windows Management Infrastructure (MI). Mi è completamente compatibile con le versioni precedenti di WMI e offre una serie di funzionalità e vantaggi che rendono più semplice che mai la progettazione e lo sviluppo di provider e client. Per altre informazioni, vedere [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Se applicabile

WMI può essere usato in tutte le Windows basate su applicazioni e risulta particolarmente utile nelle applicazioni aziendali e negli script amministrativi.

Gli amministratori di sistema possono trovare informazioni sull'uso di WMI in TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)e in vari libri su WMI. Per altre informazioni, vedere [Altre informazioni.](further-information.md)

## <a name="developer-audience"></a>Sviluppatori

WMI è progettato per i programmatori che usano C/C++, l'applicazione Microsoft Visual Basic o un linguaggio di scripting che dispone di un motore in Windows e gestisce gli oggetti di Microsoft ActiveX. Sebbene una certa familiarità con la programmazione COM sia utile, gli sviluppatori C++ che scrivono applicazioni possono trovare esempi utili per iniziare a creare un'applicazione [WMI usando C++.](creating-a-wmi-application-using-c-.md)

Per sviluppare applicazioni o provider di codice gestito in C# o Visual Basic .NET usando .NET Framework, vedere [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Molti amministratori e professionisti IT accedono a WMI tramite PowerShell. Il cmdlet Get-WMI per PowerShell consente di recuperare informazioni per un repository WMI locale o remoto. Di conseguenza, alcuni argomenti e classi, in particolare nella sezione Creazione di client [WMI,](creating-wmi-clients.md) contengono esempi di PowerShell. Per altre informazioni sull'uso di PowerShell, vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) [e Scripting con Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Requisiti di runtime

Per altre informazioni sul sistema operativo necessario per usare un elemento API o una classe WMI specifica, vedere la sezione Requisiti di ogni argomento nella documentazione di WMI.

Se un componente previsto risulta mancante, vedere [Disponibilità del sistema operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

Non è necessario scaricare o installare un SDK (Software Development) specifico per creare script o applicazioni per WMI. Esistono tuttavia alcuni strumenti di amministrazione WMI che gli sviluppatori trovano utili. Per altre informazioni, vedere la sezione Download in [Altre informazioni.](further-information.md)

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dd>

Informazioni generali su WMI.

</dd> <dt>

[Uso di WMI](using-wmi.md)
</dt> <dd>

Informazioni su come sviluppare applicazioni per l'utilizzo di WMI, incluse informazioni sugli strumenti.

</dd> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dd>

Documentazione sulle classi WMI, le classi WMI C++, l'API COM WMI, l'API di scripting e altro materiale di riferimento WMI.

</dd> </dl>

 

 
