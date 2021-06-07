---
title: La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() dalle app di Windows Store non è supportata
description: La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() dalle app di Windows Store non è supportata
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443147"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() dalle app di Windows Store non è supportata

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
Servers - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() da un'app di Windows Store non è supportata e può causare risultati imprevisti.

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

 

 