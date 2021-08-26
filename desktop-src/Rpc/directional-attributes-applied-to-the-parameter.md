---
title: Attributi direzionali applicati al parametro
description: Gli attributi direzionali \ in e \ out\ determinano come il client e il server allocano e liberano la memoria. La tabella seguente riepiloga l'effetto degli attributi direzionali sull'allocazione della memoria.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e18e34a7ea553fd5c1fd9157877a0296e403443fc490bb328f48ac4b7b2c8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073391"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Attributi direzionali applicati al parametro

Gli attributi direzionali in e out determinano il modo in cui \[ [](/windows/desktop/Midl/in) \] il client e \[ [](/windows/desktop/Midl/out-idl) \] il server allocano e liberano la memoria. La tabella seguente riepiloga l'effetto degli attributi direzionali sull'allocazione della memoria.



| Attributo direzionale    | Memoria nel client                                                                                            | Memoria nel server                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[in](/windows/desktop/Midl/in)\]       | L'applicazione client deve allocare prima della chiamata.                                                           | Alloca stub del server.                                                                                                                                  |
| \[[out](/windows/desktop/Midl/out-idl)\] | Lo stub del client viene allocato al ritorno.                                                                            | Lo stub del server alloca solo il puntatore di primo livello; L'applicazione server deve allocare tutti i puntatori incorporati. Il server alloca anche nuovi dati in base alle esigenze. |
| \[**in**, **out**\]      | L'applicazione client deve allocare i dati iniziali trasmessi al server; Lo stub client alloca dati aggiuntivi. | Lo stub del server alloca i dati iniziali trasmessi dal client; l'applicazione server alloca nuovi dati in base alle esigenze.                                        |



 

In tutti questi casi lo stub del client non libera memoria. L'applicazione client deve liberare la memoria prima che termini. Lo stub del server libera memoria quando viene restituita la chiamata di procedura remota (soggetta all'attributo \[ [ACF di](/windows/desktop/Midl/allocate) \] allocazione).

 

 