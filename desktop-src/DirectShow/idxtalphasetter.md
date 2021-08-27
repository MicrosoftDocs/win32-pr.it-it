---
description: L'interfaccia IDxtAlphaSetter imposta le proprietà sull'effetto Alpha Setter. Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering dell'effetto Alpha Setter.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interfaccia IDxtAlphaSetter (Qedit.h)
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
ms.openlocfilehash: f1cc4056733dbd0e46639a921da65e5cb2a81f3601fa1ae00624be7d92ddc0e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051931"
---
# <a name="idxtalphasetter-interface"></a>Interfaccia IDxtAlphaSetter

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`IDxtAlphaSetter`L'interfaccia imposta le proprietà sull'effetto Alpha [Setter.](alpha-setter-effect.md)

Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering dell'effetto Alpha Setter. Le applicazioni DES non devono usare questa interfaccia. Per impostare le proprietà in una transizione in DES, usare [**l'interfaccia IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Membri

**L'interfaccia IDxtAlphaSetter** eredita da **IDXEffect**. **IDxtAlphaSetter** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDxtAlphaSetter** include questi metodi.



| Metodo                                                  | Descrizione                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**get \_ Alpha**](idxtalphasetter-get-alpha.md)         | Recupera il valore alfa per l'intera immagine.<br/> |
| [**get \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Recupera la proprietà alpha ramp.<br/>              |
| [**put \_ Alpha**](idxtalphasetter-put-alpha.md)         | Specifica il valore alfa per l'intera immagine.<br/> |
| [**put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Specifica la proprietà alpha ramp.<br/>              |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




