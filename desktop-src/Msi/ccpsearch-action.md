---
description: L'azione CCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Azione CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310998"
---
# <a name="ccpsearch-action"></a>Azione CCPSearch

L'azione CCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

È necessario creare l'azione CCPSearch nella tabella [InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione dell'azione CCPSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence. L'azione CCPSearch deve precedere l'azione [RMCCPSearch](rmccpsearch-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione CCPSearch Cerca le firme dei file elencate nella tabella CCPSearch del sistema usando le tabelle seguenti nell'ordine: Signature, CompLocator, RegLocator, IniLocator e DrLocator.

Se viene determinata una firma esistente, la proprietà **CCP \_ Success** è impostata su 1 e l'azione CCPSearch termina.

L'assenza della firma dalla tabella delle firme indica una directory.

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

 

 



