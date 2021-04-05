---
title: La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata
description: La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727695"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8,1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () da un'app di Windows Store non è supportata e può causare risultati imprevisti.

## <a name="manifestations"></a>Manifestazioni

All'avvio dell'applicazione, la modalità IME è impostata sui valori predefiniti seguenti:



|          | Pannello di input software | Tastiera hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Attivato                   | Disattivato               |
| CHS, CHT | Attivato                   | Attivato                |



 

## <a name="solution"></a>Soluzione

Gli sviluppatori possono controllare la modalità IME predefinita specificando un valore dell'ambito di input per il campo.

La modalità IME per un ambito di input specificato è determinata da ogni IME. Gli sviluppatori non possono specificare la modalità IME.

## <a name="resources"></a>Risorse

-   [Enumerazione InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 