---
description: L'azione di installazione è un'azione di primo livello chiamata per installare o rimuovere i componenti.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Azione di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049852"
---
# <a name="install-action"></a>Azione di installazione

L'azione di installazione è un'azione di primo livello chiamata per installare o rimuovere i componenti. Questa azione esegue una query sulla [tabella InstallUISequence](installuisequence-table.md) e sulla [tabella InstallExecuteSequence](installexecutesequence-table.md) per l'azione da eseguire, la condizione per l'esecuzione dell'azione e il posto dell'azione nella sequenza:

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione di installazione non viene chiamata dalla sequenza della tabella delle azioni, viene passata a Windows Installer quando viene chiamato [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando '**/i**' o quando viene chiamata una funzione di installazione che può eseguire un'attività di installazione, ad esempio [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



