---
description: Sequenze di azioni suggerite per una tabella AdminUISequence di base in un database Windows Installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755399"
---
# <a name="suggested-adminuisequence"></a>AdminUISequence suggerito



| Azione                                      | Condizione | Sequenza |
|---------------------------------------------|-----------|----------|
| FatalErrorDlg                               |           | -3       |
| UserExitDlg                                 |           | -2       |
| ExitDlg                                     |           | -1       |
| PrepareDlg                                  |           | 140      |
| [CostInitialize](costinitialize-action.md) |           | 800      |
| [Filecost](filecost-action.md)             |           | 900      |
| [CostFinalize secondo](costfinalize-action.md)     |           | 1000     |
| AdminWelcomeDlg                             |           | 1230     |
| ProgressDlg                                 |           | 1280     |
| [ExecuteAction](executeaction-action.md)   |           | 1300     |



 

 

 



