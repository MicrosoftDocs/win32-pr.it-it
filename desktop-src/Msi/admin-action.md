---
description: L'azione di amministrazione è un'azione di primo livello utilizzata per eseguire installazioni amministrative.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Azione di amministrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881153"
---
# <a name="admin-action"></a>Azione di amministrazione

L'azione di amministrazione è un'azione di primo livello utilizzata per eseguire [installazioni amministrative](administrative-installation.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione di amministrazione non viene chiamata dalla sequenza della tabella delle azioni, Windows Installer esegue questa azione quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) viene chiamato con il parametro *szCommandLine* impostato su "Action = admin" o l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando "/a".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Tabella AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



