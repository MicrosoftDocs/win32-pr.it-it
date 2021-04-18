---
description: L'azione RMCCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Azione RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309455"
---
# <a name="rmccpsearch-action"></a>Azione RMCCPSearch

L'azione RMCCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

È necessario creare l'azione RMCCPSearch nella tabella [InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione di RMCCPSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Per l'azione RMCCPSearch è necessario impostare la proprietà dell' [**\_ unità CCP**](ccp-drive.md) sul percorso radice sul [*volume*](v-gly.md) rimovibile con l'installazione di uno dei prodotti idonei.

Ogni firma del file nella tabella CCPSearch viene cercata nel percorso a cui fa riferimento la proprietà dell' [**\_ unità CCP**](ccp-drive.md) usando la tabella [DrLocator](drlocator-table.md) . L'assenza della firma dalla tabella delle [firme](signature-table.md) indica una directory. Se viene determinata una firma esistente, l'azione RMCCPSearch viene terminata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



