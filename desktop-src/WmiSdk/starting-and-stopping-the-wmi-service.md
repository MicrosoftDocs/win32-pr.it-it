---
description: WMI viene eseguito come servizio con il nome visualizzato &\# 0034;Windows Management Instrumentation&0034; e il nome del servizio \# &\# 0034;winmgmt&\# 0034;.
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
ms.openlocfilehash: b22524d356bad5f23f4ca1cc8a3e7c68e69fd83f0dc38e64eba70bc1812436f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315009"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Avvio e arresto del servizio WMI

WMI viene eseguito come servizio con il nome visualizzato "Windows Management Instrumentation" e il nome del servizio "winmgmt". WMI viene eseguito automaticamente all'avvio del sistema con l'account LocalSystem. Se WMI non è in esecuzione, viene avviato automaticamente quando la prima applicazione di gestione o script richiede la connessione a uno spazio dei nomi WMI.

Molti altri servizi dipendono dal servizio WMI, a seconda della versione del sistema operativo in esecuzione nel sistema.

## <a name="starting-winmgmt-service"></a>Avvio del servizio Winmgmt

Nella procedura seguente viene descritto come avviare il servizio WMI.

**Per avviare il servizio Winmgmt**

1.  Al prompt dei comandi immettere **net** **start** **winmgmt** \[ */<switch>* \] .

    Per altre informazioni sulle opzioni disponibili, vedere [winmgmt.](winmgmt.md) Per avviare il servizio WMI, usare l'account Predefinito Administrator o un account del gruppo Administrators in esecuzione con diritti elevati. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](user-account-control-and-wmi.md)

2.  Altri servizi che dipendono dal servizio WMI, ad esempio l'host dell'agente SMS o Windows Firewall, non verranno riavviati automaticamente.

## <a name="stopping-winmgmt-service"></a>Arresto del servizio Winmgmt

Nella procedura seguente viene descritto come arrestare il servizio WMI.

**Per arrestare il servizio Winmgmt**

1.  Al prompt dei comandi immettere **net stop winmgmt**.

2.  Anche altri servizi che dipendono dal servizio WMI vengono arrestati, ad esempio l'host dell'agente SMS o Windows firewall.

## <a name="examples"></a>Esempio

TechNet Gallery contiene lo [script watchdog](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)del servizio WMI , che descrive come arrestare e riavviare il servizio winmgmt a livello di codice con PowerShell.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli strumenti di Command-Line WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



