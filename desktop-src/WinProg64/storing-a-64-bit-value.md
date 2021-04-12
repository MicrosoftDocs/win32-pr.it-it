---
title: Archiviazione di un valore a 64 bit
description: Per archiviare un valore di puntatore a 64 bit, utilizzare ULONG \_ ptr. Un \_ valore PTR ULONG è 32 bit quando viene compilato con un compilatore a 32 bit e 64 bit quando viene compilato con un compilatore a 64 bit.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- archiviazione dei valori a 64 bit programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330031"
---
# <a name="storing-a-64-bit-value"></a>Archiviazione di un valore a 64 bit

Per archiviare un valore di puntatore a 64 bit, utilizzare **ULONG \_ ptr**. Un **valore \_ ptr ULONG** è 32 bit quando viene compilato con un compilatore a 32 bit e 64 bit quando viene compilato con un compilatore a 64 bit.

Negli esempi seguenti viene usato codice reale che è stato trasferito in Windows a 64 bit. Il commento sulla procedura per rendere compatibile il codice a 64 bit è incluso.

## <a name="example-1-getting-an-address"></a>Esempio 1: recupero di un indirizzo

Il codice seguente illustra un modo portatile per ottenere un indirizzo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Uso di ULONG (metodo solo a 32 bit)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td>Uso di ULONG_PTR (metodo portatile)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a>Esempio 2: calcolo di un indirizzo

Il codice seguente illustra un modo portatile per calcolare un indirizzo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Uso di ULONG (metodo solo a 32 bit)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td>Uso di ULONG_PTR (metodo portatile)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




