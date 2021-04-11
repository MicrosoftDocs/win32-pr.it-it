---
description: WMI viene eseguito come servizio con il nome visualizzato &\# 0034; Strumentazione gestione Windows&\# 0034; e il nome del servizio &\# 0034; winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Avvio e arresto del servizio WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226819"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Avvio e arresto del servizio WMI

WMI viene eseguito come servizio con il nome visualizzato "Strumentazione gestione Windows" e il nome del servizio "WinMgmt". WMI viene eseguito automaticamente all'avvio del sistema con l'account LocalSystem. Se WMI non è in esecuzione, viene avviato automaticamente quando il primo script o un'applicazione di gestione richiede la connessione a uno spazio dei nomi WMI.

Molti altri servizi dipendono dal servizio WMI, a seconda della versione del sistema operativo in esecuzione nel sistema.

## <a name="starting-winmgmt-service"></a>Avvio del servizio WinMgmt

Nella procedura riportata di seguito viene descritto come avviare il servizio WMI.

**Per avviare il servizio WinMgmt**

1.  Al prompt dei comandi immettere **net** **Start** **WinMgmt** \[ */<switch>* \] .

    Per ulteriori informazioni sulle opzioni disponibili, vedere [WinMgmt](winmgmt.md). Utilizzare l'account Administrator predefinito o un account del gruppo Administrators che esegue con diritti elevati per avviare il servizio WMI. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).

2.  Altri servizi che dipendono dal servizio WMI, ad esempio host agenti di SMS o Windows Firewall, non verranno riavviati automaticamente.

## <a name="stopping-winmgmt-service"></a>Arresto del servizio WinMgmt

Nella procedura riportata di seguito viene descritto come arrestare il servizio WMI.

**Per arrestare il servizio WinMgmt**

1.  Al prompt dei comandi, immettere **net stop winmgmt**.

2.  Anche altri servizi che dipendono dal servizio WMI si interrompono, ad esempio host agenti di SMS o Windows Firewall.

## <a name="examples"></a>Esempio

La raccolta TechNet contiene lo [script del watchdog del servizio WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), che descrive come arrestare e riavviare il servizio WinMgmt a livello di codice con PowerShell.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo degli strumenti di Command-Line WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



