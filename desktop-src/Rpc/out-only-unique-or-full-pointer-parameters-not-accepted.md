---
title: Out-Only parametri puntatore univoci o completi non accettati
description: I puntatori univoci o completi che sono \ out\ -only non sono accettati dal compilatore MIDL. Tali specifiche causano la generazione di un messaggio di errore da parte del compilatore MIDL.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9511c21045892eb7a5b3230d8f0180578b489b06b5b5402fb0b11f6a3ff31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927570"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only parametri puntatore univoci o completi non accettati

I puntatori univoci o completi che sono \[ [out](/windows/desktop/Midl/out-idl) \] -only non vengono accettati dal compilatore MIDL. Tali specifiche causano la generazione di un messaggio di errore da parte del compilatore MIDL.

Lo stub del server generato automaticamente deve allocare memoria per il riferimento del puntatore in modo che l'applicazione server possa archiviare i dati in tale area di memoria. In base alla definizione di un **\[ parametro out \]**-only, nessuna informazione sul parametro viene trasmessa dal client al server. Nel caso di un puntatore univoco, che può assumere il valore null, lo stub del server non dispone di informazioni sufficienti per duplicare correttamente il puntatore univoco nello spazio degli indirizzi del server, né contiene informazioni sul fatto che il puntatore punti a un indirizzo valido o se deve essere impostato su Null. Pertanto, questa combinazione non è consentita.

Anziché out , unique o out , i puntatori ptr, usare in , out , unique o \[  [](/windows/desktop/Midl/unique) \] \[  [](/windows/desktop/Midl/ptr) \] \[    \] \[ **in**, **out**, **puntatori ptr** \] o usare un altro livello di riferimento indiretto, ad esempio un puntatore di riferimento che punta al puntatore univoco o completo valido.

 

 