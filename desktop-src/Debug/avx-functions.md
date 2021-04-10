---
description: Funzioni di Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: Funzioni AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225517"
---
# <a name="avx-functions"></a>Funzioni AVX

Di seguito sono riportate le funzioni di Intel AVX.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                   | Descrizione                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**CopyContext**](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | Copia una struttura del contesto di origine (incluso qualsiasi XState) in una struttura del contesto di destinazione inizializzata.<br/>         |
| [**GetEnabledXStateFeatures**](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | Ottiene una maschera delle funzionalità XState abilitate nei processori x86 o x64.<br/>                                                    |
| [**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | Restituisce la maschera delle funzionalità XState impostate all'interno di una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .<br/>                        |
| [**InitializeContext**](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | Inizializza una struttura di [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) all'interno di un buffer con le dimensioni e l'allineamento necessari.<br/>       |
| [**LocateXStateFeature**](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | Recupera un puntatore allo stato del processore per una funzionalità XState all'interno di una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .<br/> |
| [**SetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | Imposta la maschera delle funzionalità XState impostate all'interno di una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .<br/>                             |



 

 

 




