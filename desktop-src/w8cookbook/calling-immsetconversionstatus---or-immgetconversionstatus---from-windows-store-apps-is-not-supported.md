---
title: La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() da app Windows Store non è supportata
description: La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() da app Windows Store non è supportata
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9950bc008ce96d6c0a80a6090c3312057a12c4a7a1f64a5563625a518831c27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348571"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() da app Windows Store non è supportata

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
Server - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() da un'app Windows Store non è supportata e può causare risultati imprevisti.

## <a name="manifestations"></a>Manifestazioni

All'avvio dell'applicazione, la modalità IME è impostata sul valore predefinito seguente:



| &nbsp;   | Pannello di input software | Tastiera hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Attivato                   | Disattivato               |
| CHS, CHT | On                   | On                |



 

## <a name="solution"></a>Soluzione

Gli sviluppatori possono controllare la modalità IME predefinita specificando un valore di ambito di input per il campo.

La modalità IME per un ambito di input specificato è determinata da ogni IME. Gli sviluppatori non possono specificare la modalità IME.

## <a name="resources"></a>Risorse

-   [Enumerazione InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 