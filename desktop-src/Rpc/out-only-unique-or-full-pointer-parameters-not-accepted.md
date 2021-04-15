---
title: Out-Only parametri del puntatore univoco o completo non accettati
description: I puntatori univoci o completi che sono \ out solo non sono accettati dal compilatore MIDL. Tali specifiche fanno sì che il compilatore MIDL generi un messaggio di errore.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516977"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only parametri del puntatore univoco o completo non accettati

I puntatori univoci o completi \[ [](/windows/desktop/Midl/out-idl) \] non sono accettati dal compilatore MIDL. Tali specifiche fanno sì che il compilatore MIDL generi un messaggio di errore.

Lo stub del server generato automaticamente deve allocare memoria per il referente del puntatore, in modo che l'applicazione server possa archiviare i dati nell'area di memoria. In base alla definizione di un parametro di sola **\[ uscita \]**, nessuna informazione sul parametro viene trasmessa dal client al server. Nel caso di un puntatore univoco, che può assumere il valore null, lo stub del server non dispone di informazioni sufficienti per duplicare correttamente il puntatore univoco nello spazio degli indirizzi del server, né lo stub contiene informazioni sul fatto che il puntatore punti a un indirizzo valido o se deve essere impostato su null. Questa combinazione non è pertanto consentita.

Invece di \[ **out**, [Unique](/windows/desktop/Midl/unique) \] o \[ **out**, [](/windows/desktop/Midl/ptr) \] puntatori PTR, utilizzare \[ **in**, **out**, **Unique** \] o \[ **in**, **out**, **ptr** \] puntatori o utilizzare un altro livello di riferimento indiretto, ad esempio un puntatore di riferimento che punta al puntatore univoco o completo valido.

 

 