---
description: WMI viene eseguito come servizio con il nome visualizzato &0034;strumentazione di gestione Windows&0034; e il nome del servizio \# \# &\# 0034;winmgmt&\# 0034;.
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
ms.openlocfilehash: 6a60d6ed17c6a5524af2a9bb54f386a325f63c10
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880246"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Avvio e arresto del servizio WMI

WMI viene eseguito come servizio con il nome visualizzato "Windows Management Instrumentation" e il nome del servizio "winmgmt". WMI viene eseguito automaticamente all'avvio del sistema con l'account LocalSystem. Se WMI non è in esecuzione, viene avviato automaticamente quando la prima applicazione di gestione o script richiede la connessione a uno spazio dei nomi WMI.

Diversi altri servizi dipendono dal servizio WMI, a seconda della versione del sistema operativo in esecuzione.

## <a name="starting-winmgmt-service"></a>Avvio del servizio Winmgmt

La procedura seguente descrive come avviare il servizio WMI.

**Per avviare il servizio Winmgmt**

1.  Al prompt dei comandi immettere **net** **start** **winmgmt** \[ */ &lt; switch &gt;* \] .

    Per altre informazioni sulle opzioni disponibili, vedere [winmgmt](winmgmt.md). Per avviare il servizio WMI si usa l'account Administrator predefinito o un account del gruppo Administrators in esecuzione con diritti elevati. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](user-account-control-and-wmi.md)

2.  Altri servizi dipendenti dal servizio WMI, ad esempio l'host agente SMS o Windows Firewall, non verranno riavviati automaticamente.

## <a name="stopping-winmgmt-service"></a>Arresto del servizio Winmgmt

La procedura seguente descrive come arrestare il servizio WMI.

**Per arrestare il servizio Winmgmt**

1.  Al prompt dei comandi immettere **net stop winmgmt**.

2.  Anche altri servizi dipendenti dal servizio WMI vengono arrestati, ad esempio l'host dell'agente SMS o Windows Firewall.

## <a name="examples"></a>Esempio

La raccolta TechNet contiene lo [script watchdog](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)del servizio WMI , che descrive come arrestare e riavviare il servizio winmgmt a livello di codice con PowerShell.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli strumenti Command-Line WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



