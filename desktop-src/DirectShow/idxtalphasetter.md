---
description: L'interfaccia IDxtAlphaSetter imposta le proprietà sull'effetto Setter alfa. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando viene eseguito il rendering dell'effetto Alpha Setter.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interfaccia IDxtAlphaSetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330175"
---
# <a name="idxtalphasetter-interface"></a>Interfaccia IDxtAlphaSetter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IDxtAlphaSetter` interfaccia imposta le proprietà sull'effetto del [Setter alfa](alpha-setter-effect.md) .

Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando viene eseguito il rendering dell'effetto Alpha Setter. Non è necessario che le applicazioni DES usino questa interfaccia. Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membri

L'interfaccia **IDxtAlphaSetter** eredita da **IDXEffect**. **IDxtAlphaSetter** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDxtAlphaSetter** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**Ottieni \_ alfa**](idxtalphasetter-get-alpha.md)         | Recupera il valore alfa per l'intera immagine.<br/> |
| [**ottenere \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Recupera la proprietà della rampa alfa.<br/>              |
| [**Inserisci \_ Alpha**](idxtalphasetter-put-alpha.md)         | Specifica il valore alfa per l'intera immagine.<br/> |
| [**Inserisci \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Specifica la proprietà della rampa alfa.<br/>              |



 

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



 

 




