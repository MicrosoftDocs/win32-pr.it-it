---
description: L'interfaccia IDxtKey imposta le proprietà per la transizione key. Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering della transizione della chiave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interfaccia IDxtKey (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d967d15dededf879ffd08671aac00e7892aa8ad2f2c1a39ce478f7f9f3e4db90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792361"
---
# <a name="idxtkey-interface"></a>Interfaccia IDxtKey

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`IDxtKey`L'interfaccia imposta le proprietà per la [transizione](key-transition.md) key.

Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering della transizione della chiave. Non è necessario che le applicazioni DES usino questa interfaccia. Per impostare le proprietà in una transizione in DES, usare [**l'interfaccia IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Membri

**L'interfaccia IDxtKey** eredita da **IDXEffect.** **IDxtKey** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDxtKey** include questi metodi.



| Metodo                                            | Descrizione                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**get \_ Hue**](idxtkey-get-hue.md)               | Recupera il valore della tonalità su cui eseguire la chiave.<br/>                                    |
| [**get \_ Invert**](idxtkey-get-invert.md)         | Recupera un valore booleano che indica se l'operazione di chiave è invertita.<br/> |
| [**get \_ KeyType**](idxtkey-get-keytype.md)       | Recupera il tipo di chiave.<br/>                                                  |
| [**get \_ Luminance**](idxtkey-get-luminance.md)   | Recupera il valore di luminance su cui eseguire la chiave.<br/>                              |
| [**ottenere \_ RGB**](idxtkey-get-rgb.md)               | Recupera il colore RGB su cui eseguire la chiave.<br/>                                    |
| [**get \_ Similarity**](idxtkey-get-similarity.md) | Recupera l'intervallo di dati di colore che diventa trasparente.<br/>                 |
| [**put \_ Hue**](idxtkey-put-hue.md)               | Specifica il valore della tonalità su cui eseguire la chiave.<br/>                                    |
| [**put \_ Invert**](idxtkey-put-invert.md)         | Specifica se l'operazione della chiave è invertita.<br/>                            |
| [**put \_ KeyType**](idxtkey-put-keytype.md)       | Specifica il tipo di chiave.<br/>                                                  |
| [**put \_ Luminance**](idxtkey-put-luminance.md)   | Specifica il valore di luminance su cui eseguire la chiave.<br/>                              |
| [**put \_ RGB**](idxtkey-put-rgb.md)               | Specifica il colore RGB su cui eseguire la chiave.<br/>                                    |
| [**put \_ Similarity**](idxtkey-put-similarity.md) | Specifica l'intervallo di dati di colore che diventa trasparente.<br/>                 |



 

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



 

 




