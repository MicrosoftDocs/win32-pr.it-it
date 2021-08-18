---
description: L'interfaccia IDxtCompositor imposta le proprietà per la transizione Compositor. Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering della transizione Compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interfaccia IDxtCompositor (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd59f62a4382ae6023a18792ce3547f67b49c9e8ae49e9de7c9c8409bccd788d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997696"
---
# <a name="idxtcompositor-interface"></a>Interfaccia IDxtCompositor

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`IDxtCompositor`L'interfaccia imposta le proprietà sulla transizione [Compositor.](compositor-transition.md)

Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering della transizione Compositor. Le applicazioni DES non devono usare questa interfaccia. Per impostare le proprietà in una transizione in DES, usare [**l'interfaccia IPropertySetter.**](ipropertysetter.md)

La transizione Compositor composita un'immagine in primo piano su un'immagine di sfondo. Il *rettangolo di* origine definisce la sezione dell'immagine in primo piano composta. Il *rettangolo di* destinazione definisce la sezione dell'immagine di sfondo che riceve l'immagine in primo piano. Il diagramma seguente illustra questi rettangoli.

![Proprietà della transizione compositor](images/compmeasure.png)

## <a name="members"></a>Membri

**L'interfaccia IDxtCompositor** eredita da **IDXEffect.** **IDxtCompositor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDxtCompositor** include questi metodi.



| Metodo                                                   | Descrizione                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**get \_ Height**](idxtcompositor-get-height.md)         | Recupera l'altezza del rettangolo di destinazione.<br/>            |
| [**get \_ OffsetX**](idxtcompositor-get-offsetx.md)       | Recupera l'offset orizzontale del rettangolo di destinazione.<br/> |
| [**get \_ OffsetY**](idxtcompositor-get-offsety.md)       | Recupera l'offset verticale del rettangolo di destinazione.<br/>   |
| [**get \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Recupera l'altezza del rettangolo di origine.<br/>            |
| [**get \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Recupera l'offset orizzontale del rettangolo di origine.<br/> |
| [**get \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Recupera l'offset verticale del rettangolo di origine.<br/>   |
| [**get \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Recupera la larghezza del rettangolo di origine.<br/>             |
| [**get \_ Width**](idxtcompositor-get-width.md)           | Recupera la larghezza del rettangolo di destinazione.<br/>             |
| [**put \_ Height**](idxtcompositor-put-height.md)         | Specifica l'altezza del rettangolo di destinazione.<br/>            |
| [**put \_ OffsetX**](idxtcompositor-put-offsetx.md)       | Specifica l'offset orizzontale del rettangolo di destinazione.<br/> |
| [**put \_ OffsetY**](idxtcompositor-put-offsety.md)       | Specifica l'offset verticale del rettangolo di destinazione.<br/>   |
| [**put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Specifica l'altezza del rettangolo di origine.<br/>            |
| [**put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Specifica l'offset orizzontale del rettangolo di origine.<br/> |
| [**put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Specifica l'offset verticale del rettangolo di origine.<br/>   |
| [**put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Specifica la larghezza del rettangolo di origine.<br/>             |
| [**Put \_ Width**](idxtcompositor-put-width.md)           | Specifica la larghezza del rettangolo di destinazione.<br/>             |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




