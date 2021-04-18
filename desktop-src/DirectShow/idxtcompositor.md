---
description: L'interfaccia IDxtCompositor imposta le proprietà nella transizione del Compositor. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione del Compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interfaccia IDxtCompositor (qedit. h)
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
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331513"
---
# <a name="idxtcompositor-interface"></a>Interfaccia IDxtCompositor

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IDxtCompositor` interfaccia imposta le proprietà nella transizione del [compositor](compositor-transition.md) .

Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione del Compositor. Non è necessario che le applicazioni DES usino questa interfaccia. Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

La transizione del Compositor compone un'immagine di primo piano su un'immagine di sfondo. Il *rettangolo di origine* definisce la sezione dell'immagine in primo piano composta. Il *rettangolo di destinazione* definisce la sezione dell'immagine di sfondo che riceve l'immagine in primo piano. Il diagramma seguente illustra questi rettangoli.

![Proprietà di transizione del Compositor](images/compmeasure.png)

## <a name="members"></a>Membri

L'interfaccia **IDxtCompositor** eredita da **IDXEffect**. **IDxtCompositor** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDxtCompositor** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**Ottieni \_ altezza**](idxtcompositor-get-height.md)         | Recupera l'altezza del rettangolo di destinazione.<br/>            |
| [**ottenere \_ offsetX**](idxtcompositor-get-offsetx.md)       | Recupera l'offset orizzontale del rettangolo di destinazione.<br/> |
| [**Ottieni \_ offset**](idxtcompositor-get-offsety.md)       | Recupera l'offset verticale del rettangolo di destinazione.<br/>   |
| [**ottenere \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Recupera l'altezza del rettangolo di origine.<br/>            |
| [**ottenere \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Recupera l'offset orizzontale del rettangolo di origine.<br/> |
| [**ottenere \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Recupera l'offset verticale del rettangolo di origine.<br/>   |
| [**ottenere \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Recupera la larghezza del rettangolo di origine.<br/>             |
| [**Ottieni \_ larghezza**](idxtcompositor-get-width.md)           | Recupera la larghezza del rettangolo di destinazione.<br/>             |
| [**\_altezza put**](idxtcompositor-put-height.md)         | Specifica l'altezza del rettangolo di destinazione.<br/>            |
| [**Inserisci \_ offsetX**](idxtcompositor-put-offsetx.md)       | Specifica l'offset orizzontale del rettangolo di destinazione.<br/> |
| [**Inserisci \_ offset**](idxtcompositor-put-offsety.md)       | Specifica l'offset verticale del rettangolo di destinazione.<br/>   |
| [**Inserisci \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Specifica l'altezza del rettangolo di origine.<br/>            |
| [**Inserisci \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Specifica l'offset orizzontale del rettangolo di origine.<br/> |
| [**Inserisci \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Specifica l'offset verticale del rettangolo di origine.<br/>   |
| [**Inserisci \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Specifica la larghezza del rettangolo di origine.<br/>             |
| [**Inserisci \_ larghezza**](idxtcompositor-put-width.md)           | Specifica la larghezza del rettangolo di destinazione.<br/>             |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 




