---
description: Strumentazione gestione Windows (WMI) è l'infrastruttura per i dati e le operazioni di gestione nei sistemi operativi basati su Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Strumentazione gestione Windows (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310332"
---
# <a name="windows-management-instrumentation"></a>Strumentazione gestione Windows (WMI)

## <a name="purpose"></a>Scopo

Strumentazione gestione Windows (WMI) è l'infrastruttura per i dati e le operazioni di gestione nei sistemi operativi basati su Windows. È possibile scrivere script o applicazioni WMI per automatizzare le attività amministrative sui computer remoti, ma WMI fornisce anche i dati di gestione ad altre parti del sistema operativo e dei prodotti, ad esempio System Center Operations Manager, in precedenza Microsoft Operations Manager (MOM) o Gestione remota Windows ([WinRM](/windows/desktop/WinRM/portal)).

> [!Note]  
> La seguente documentazione è destinata agli sviluppatori e agli amministratori IT. Se si è un utente finale che ha riscontrato un messaggio di errore relativo a WMI, è necessario passare a [supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore. Per ulteriori informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere la pagina relativa al [funzionamento di WMI.](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI è completamente supportato da Microsoft; Tuttavia, la versione più recente del controllo e dello scripting amministrativo è disponibile tramite l'infrastruttura di gestione Windows (MI). MI è completamente compatibile con le versioni precedenti di WMI e offre una serie di funzionalità e vantaggi che semplificano la progettazione e lo sviluppo di provider e client. Per ulteriori informazioni, vedere [Windows Management Infrastructure (mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Se applicabile

WMI può essere utilizzato in tutte le applicazioni basate su Windows ed è particolarmente utile nelle applicazioni aziendali e negli script amministrativi.

Gli amministratori di sistema possono trovare informazioni sull'utilizzo di WMI presso TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)e in diversi libri su WMI. Per ulteriori informazioni, vedere [ulteriori informazioni](further-information.md).

## <a name="developer-audience"></a>Sviluppatori

WMI è progettato per i programmatori che utilizzano C/C++, l'applicazione Microsoft Visual Basic o un linguaggio di scripting che dispone di un motore di Windows e gestisce gli oggetti ActiveX Microsoft. Sebbene sia utile una certa familiarità con la programmazione COM, gli sviluppatori C++ che scrivono applicazioni possono trovare ottimi esempi per iniziare a [creare un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md).

Per sviluppare applicazioni o provider di codice gestito in C# o Visual Basic .NET usando il .NET Framework, vedere [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Molti amministratori e professionisti IT accedono a WMI tramite PowerShell. Il cmdlet Get-WMI per PowerShell consente di recuperare informazioni per un repository WMI locale o remoto. Di conseguenza, una serie di argomenti e classi, soprattutto nella sezione [creazione di client WMI](creating-wmi-clients.md) , contiene esempi di PowerShell. Per altre informazioni sull'uso di PowerShell, vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) e creazione di [script con Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Requisiti di runtime

Per ulteriori informazioni sul sistema operativo richiesto per l'utilizzo di un elemento API specifico o di una classe WMI, vedere la sezione requisiti di ogni argomento nella documentazione di WMI.

Se un componente previsto risulta mancante, vedere [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).

Non è necessario scaricare o installare uno specifico SDK (Software Development) per creare script o applicazioni per WMI. Tuttavia, sono disponibili alcuni strumenti di amministrazione WMI utili per gli sviluppatori. Per ulteriori informazioni, vedere la sezione Download in [ulteriori informazioni](further-information.md).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dd>

Informazioni generali su WMI.

</dd> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> <dd>

Informazioni sullo sviluppo di applicazioni per l'utilizzo di WMI, incluse informazioni sugli strumenti di.

</dd> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dd>

Documentazione sulle classi WMI, le classi C++ WMI, l'API COM WMI, l'API di scripting e altro materiale di riferimento WMI.

</dd> </dl>

 

 
