---
description: L'azione RMCCPSearch usa le firme di file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Azione RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d18431a6806d055c824bf51331d6390a6f669100aa9a33db9665b9d7b37008c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625900"
---
# <a name="rmccpsearch-action"></a>Azione RMCCPSearch

L'azione RMCCPSearch usa le firme di file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

È necessario creare l'azione RMCCPSearch nella [tabella InstallUISequence](installuisequence-table.md) e [nella tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione di RMCCPSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione RMCCPSearch richiede che la proprietà [**CCP \_ DRIVE**](ccp-drive.md) sia impostata sul percorso radice del [*volume*](v-gly.md) rimovibile che include l'installazione per uno dei prodotti idonei.

Ogni firma di file nella tabella CCPSearch viene cercata nel percorso a cui fa riferimento la proprietà [**CCP \_ DRIVE**](ccp-drive.md) usando la [tabella DrLocator.](drlocator-table.md) L'assenza della firma dalla [tabella Signature](signature-table.md) indica una directory. Se si determina l'esistenza di una firma, l'azione RMCCPSearch termina.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



