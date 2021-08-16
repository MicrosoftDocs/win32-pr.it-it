---
description: L'azione ADMIN è un'azione di primo livello usata per eseguire installazioni amministrative.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Azione ADMIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785bd69a8de7da1df9a812f7e89d589b6e939b3eedd6b3cecb66bf86407636cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145934"
---
# <a name="admin-action"></a>Azione ADMIN

L'azione ADMIN è un'azione di primo livello usata per eseguire [installazioni amministrative.](administrative-installation.md)

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione ADMIN non viene chiamata dall'interno della sequenza di tabella delle azioni. Il programma di installazione di Windows esegue questa azione quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) viene chiamato con il parametro *szCommandLine* impostato su "ACTION=ADMIN" o il Msiexec.exe eseguibile della riga di comando viene chiamato con l'opzione della riga di comando '/a'.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Tabella AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



