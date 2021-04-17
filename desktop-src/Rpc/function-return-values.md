---
title: Valori restituiti dalla funzione
description: I valori restituiti dalla funzione sono simili ai parametri \ out solo perché i dati non sono forniti dall'applicazione client.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300329"
---
# <a name="function-return-values"></a>Valori restituiti dalla funzione

I valori restituiti dalla funzione sono simili ai parametri **\[ out \]**-only perché i dati non sono forniti dall'applicazione client. Tuttavia, vengono gestiti in modo diverso. A differenza dei parametri di sola **\[ uscita \]**, non è necessario che siano puntatori. La procedura remota può restituire qualsiasi tipo di dati valido ad eccezione dei puntatori di riferimento e delle unioni non incapsulate.

È tuttavia consigliabile utilizzare un parametro **\[ out \]** anziché un valore restituito per tipi di dati complessi. Quando si restituiscono tipi di dati complessi, il compilatore MIDL genera uno stub in modalità/OS. Di conseguenza, tutte le informazioni di controllo degli errori recenti fornite da/Robust vengono perse.

I valori restituiti dalla funzione che sono tipi di puntatore vengono allocati dallo stub client con una chiamata a [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). Di conseguenza, è possibile applicare solo l'attributo puntatore univoco o completo a un tipo restituito dalla funzione puntatore.

 

 