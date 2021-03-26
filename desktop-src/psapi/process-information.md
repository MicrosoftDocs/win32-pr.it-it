---
title: Informazioni sul processo
description: Il sistema gestisce un elenco di processi in esecuzione. È possibile recuperare gli identificatori per questi processi chiamando la funzione EnumProcesses. Questa funzione riempie una matrice di valori DWORD con gli identificatori di tutti i processi nel sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338031"
---
# <a name="process-information"></a>Informazioni sul processo

Il sistema gestisce un elenco di processi in esecuzione. È possibile recuperare gli identificatori per questi processi chiamando la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Questa funzione riempie una matrice di valori **DWORD** con gli identificatori di tutti i processi nel sistema.

Molte funzioni in PSAPI richiedono un handle di processo. Per ottenere un handle di processo per un processo in esecuzione, passare il relativo identificatore di processo (ottenuto da [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) alla funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . Ricordare di chiamare la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) al termine dell'handle di processo.

 

 