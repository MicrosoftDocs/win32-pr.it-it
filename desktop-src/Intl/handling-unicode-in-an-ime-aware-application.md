---
description: Gestione di Unicode in un'applicazione IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Gestione di Unicode in un'applicazione IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319500"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Gestione di Unicode in un'applicazione IME-Aware

Per IMM e la relativa gestione di Unicode sono necessari due problemi. Il primo problema è che le versioni Unicode delle funzioni di IMM recuperano la dimensione di un buffer in byte invece di caratteri Unicode a 16 bit. Il secondo problema è che IMM recupera in genere i caratteri Unicode, anziché i caratteri DBCS, nei messaggi [**WM \_ char**](../inputdev/wm-char.md) e [**WM \_ IME \_ char**](wm-ime-char.md) .

Windows supporta un'interfaccia Unicode per IMM, oltre all'interfaccia ANSI supportata originariamente.

Le applicazioni devono usare [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) per fare in modo che i messaggi di tipo char [**WM \_**](../inputdev/wm-char.md) e [**WM \_ \_ IME**](wm-ime-char.md) recuperino i caratteri Unicode anziché i caratteri DBCS nel parametro *wParam* .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di gestione metodi di input](using-input-method-manager.md)
</dt> </dl>

 

 
