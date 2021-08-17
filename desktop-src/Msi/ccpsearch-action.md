---
description: L'azione CCPSearch usa le firme di file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Azione CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201af22dd557541825dcf2c47f06e7cf67cd8785fa85e0b78a28c25a570ffc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145694"
---
# <a name="ccpsearch-action"></a>Azione CCPSearch

L'azione CCPSearch usa le firme di file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

È necessario creare l'azione CCPSearch nella [tabella InstallUISequence](installuisequence-table.md) e [nella tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione dell'azione CCPSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence. L'azione CCPSearch deve essere eseguita prima [dell'azione RMCCPSearch.](rmccpsearch-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione CCPSearch cerca le firme di file elencate nella tabella CCPSearch del sistema usando le tabelle seguenti nell'ordine: Signature, CompLocator, RegLocator, IniLocator e DrLocator.

Se si determina l'esistenza di una firma, la proprietà **CCP \_ Success** viene impostata su 1 e l'azione CCPSearch termina.

L'assenza della firma dalla tabella Signature indica una directory.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[CCPSearch](ccpsearch-table.md)
</dt> <dt>

[Firma](signature-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



