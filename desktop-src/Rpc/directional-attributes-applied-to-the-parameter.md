---
title: Attributi direzionali applicati al parametro
description: Gli attributi direzionali \ in \ e \ out \ determinano il modo in cui il client e il server allocano e liberano memoria. Nella tabella seguente sono riepilogati gli effetti degli attributi direzionali nell'allocazione di memoria.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300250"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Attributi direzionali applicati al parametro

Gli attributi direzionali \[ [in](/windows/desktop/Midl/in) \] e \[ [out](/windows/desktop/Midl/out-idl) \] determinano il modo in cui il client e il server allocano e liberano memoria. Nella tabella seguente sono riepilogati gli effetti degli attributi direzionali nell'allocazione di memoria.



| Attributo direzionale    | Memoria sul client                                                                                            | Memoria nel server                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[in](/windows/desktop/Midl/in)\]       | L'applicazione client deve allocare prima della chiamata.                                                           | Lo stub del server alloca.                                                                                                                                  |
| \[in [uscita](/windows/desktop/Midl/out-idl)\] | Lo stub client alloca al ritorno.                                                                            | Stub Server alloca solo il puntatore di primo livello. l'applicazione server deve allocare tutti i puntatori incorporati. Il server alloca inoltre i nuovi dati in base alle esigenze. |
| \[**in** **uscita**\]      | L'applicazione client deve allocare i dati iniziali trasmessi al server; Stub client alloca dati aggiuntivi. | Stub Server alloca i dati iniziali trasmessi dal client; l'applicazione server alloca nuovi dati in base alle esigenze.                                        |



 

In tutti questi casi lo stub del client non libera la memoria. L'applicazione client deve liberare la memoria prima di terminare. Lo stub del server libera memoria quando la chiamata di procedura remota restituisce (soggetto all' \[ attributo di [allocazione](/windows/desktop/Midl/allocate) di \] ACF).

 

 