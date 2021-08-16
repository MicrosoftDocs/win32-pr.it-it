---
description: L'azione INSTALL è un'azione di primo livello chiamata per installare o rimuovere componenti.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Azione INSTALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5f648084b7386465f6bb59dd6b523cb51489e4cb83677c0b5cb47fe845be42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811001"
---
# <a name="install-action"></a>Azione INSTALL

L'azione INSTALL è un'azione di primo livello chiamata per installare o rimuovere componenti. Questa azione esegue una query nella tabella [InstallUISequence](installuisequence-table.md) e nella tabella [InstallExecuteSequence](installexecutesequence-table.md) per l'azione da eseguire, la condizione per l'esecuzione dell'azione e la posizione dell'azione nella sequenza:

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione INSTALL non viene chiamata dall'interno della sequenza di tabella delle azioni, viene passata al programma di installazione di Windows quando viene chiamato [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o il Msiexec.exe eseguibile della riga di comando viene chiamato con l'opzione della riga di comando **'/i'** o quando viene chiamata qualsiasi funzione del programma di installazione che può eseguire un'attività di installazione, ad esempio [**MsiConfigureFeature,**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile.**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)

 

 



