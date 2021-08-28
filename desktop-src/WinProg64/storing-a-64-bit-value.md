---
title: Archiviazione di un valore a 64 bit
description: Per archiviare un valore del puntatore a 64 bit, usare ULONG \_ PTR. Un valore ULONG PTR è a 32 bit quando viene compilato con un compilatore a 32 bit e a 64 bit quando viene compilato con un \_ compilatore a 64 bit.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- archiviazione di valori a 64 bit a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469068"
---
# <a name="storing-a-64-bit-value"></a>Archiviazione di un valore a 64 bit

Per archiviare un valore del puntatore a 64 bit, usare **ULONG \_ PTR.** Un **valore \_ ULONG PTR** è a 32 bit quando viene compilato con un compilatore a 32 bit e a 64 bit quando viene compilato con un compilatore a 64 bit.

Negli esempi seguenti viene utilizzato codice reale che è stato portato a un Windows a 64 bit. Sono inclusi commenti sui passaggi per rendere il codice compatibile a 64 bit.

## <a name="example-1-getting-an-address"></a>Esempio 1: Recupero di un indirizzo

Il codice seguente illustra un modo portabile per ottenere un indirizzo.




| | | Uso di ULONG (metodo solo a 32 bit) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | | Uso ULONG_PTR (metodo portabile) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>Esempio 2: Calcolo di un indirizzo

Nel codice seguente viene illustrato un modo portabile per calcolare un indirizzo.




| | | Uso di ULONG (metodo solo a 32 bit) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | | Uso ULONG_PTR (metodo portabile) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




