---
description: L'interfaccia IAMTimelineTrans fornisce metodi per la modifica delle transizioni in servizi di modifica DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interfaccia IAMTimelineTrans (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332973"
---
# <a name="iamtimelinetrans-interface"></a>Interfaccia IAMTimelineTrans

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineTrans` interfaccia fornisce metodi per la modifica delle transizioni nei [servizi di modifica DirectShow](directshow-editing-services.md) (des). Una transizione è una progressione tra un livello video e la composita sottoposta a rendering di tutti i livelli video con una priorità più bassa. È possibile aggiungere una transizione a qualsiasi oggetto sequenza temporale che espone l'interfaccia [**IAMTimelineTransable**](iamtimelinetransable.md) . Per impostare le proprietà di una transizione, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

L'oggetto di transizione DES è effettivamente un wrapper per un oggetto Transform di DirectX. Qualsiasi oggetto di trasformazione DirectX a 2 input può essere usato per implementare l'effetto visivo per la transizione. Microsoft non supporta più lo sviluppo di oggetti di trasformazione DirectX di terze parti. Per specificare l'oggetto di trasformazione DirectX per una transizione, chiamare il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Per creare un oggetto di transizione, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con la sequenza temporale del valore \_ principale \_ Transition del tipo \_ . È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l' `IAMTimelineTrans` interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineTrans** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrans** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineTrans** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GetCutPoint**](iamtimelinetrans-getcutpoint.md)     | Recupera il punto di taglio.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Recupera il punto di taglio come valore [**REFTIME**](reftime.md) .<br/>             |
| [**GetCutsOnly**](iamtimelinetrans-getcutsonly.md)     | Determina se viene eseguito il rendering della transizione come taglia.<br/>                     |
| [**GetSwapInputs**](iamtimelinetrans-getswapinputs.md) | Recupera un valore che indica se gli input di transizione vengono scambiati.<br/> |
| [**SetCutPoint**](iamtimelinetrans-setcutpoint.md)     | Imposta il punto di taglio.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Imposta il punto di taglio come valore [**REFTIME**](reftime.md) .<br/>                  |
| [**SetCutsOnly**](iamtimelinetrans-setcutsonly.md)     | Specifica se viene eseguito il rendering della transizione come taglia.<br/>                      |
| [**SetSwapInputs**](iamtimelinetrans-setswapinputs.md) | Specifica se gli input di transizione vengono scambiati.<br/>                        |



 

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
