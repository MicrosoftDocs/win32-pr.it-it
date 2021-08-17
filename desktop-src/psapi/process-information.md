---
title: Informazioni sul processo
description: Il sistema gestisce un elenco di processi in esecuzione. È possibile recuperare gli identificatori per questi processi chiamando la funzione EnumProcesses. Questa funzione riempie una matrice di valori DWORD con gli identificatori di tutti i processi nel sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094892"
---
# <a name="process-information"></a>Informazioni sul processo

Il sistema gestisce un elenco di processi in esecuzione. È possibile recuperare gli identificatori per questi processi chiamando la [**funzione EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Questa funzione riempie una matrice **di valori DWORD** con gli identificatori di tutti i processi nel sistema.

Molte funzioni in PSAPI richiedono un handle di processo. Per ottenere un handle di processo per un processo in esecuzione, passare il relativo identificatore di processo (ottenuto da [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) alla [**funzione OpenProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) Ricordarsi di chiamare [**la funzione CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) al termine dell'handle del processo.

 

 