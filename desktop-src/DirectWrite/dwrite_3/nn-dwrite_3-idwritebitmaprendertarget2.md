---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che possono essere usati per il rendering dei glifi.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: 482aff4e2b9fbf03a89a15a7e38cc07d7542362b
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955034"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>Interfaccia IDWriteBitmapRenderTarget2 (dwrite_3.h)

Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che possono essere usati per il rendering dei glifi.

> [!IMPORTANT]
> Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md) DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme. Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore.](/windows/win32/directwrite/dwritecore-overview)

## <a name="inheritance"></a>Ereditarietà

**L'interfaccia IDWriteBitmapRenderTarget2** eredita da [IDWriteBitmapRenderTarget1.](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)

## <a name="methods"></a>Metodi

**L'interfaccia IDWriteBitmapRenderTarget2** include questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2::GetBitmapData](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | Recupera i dati pixel da una destinazione di rendering bitmap. |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, Project Reunion [app Win32] |
| **Intestazione** | dwrite_3.h (includere dwrite_core.h) |
