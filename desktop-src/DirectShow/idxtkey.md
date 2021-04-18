---
description: L'interfaccia IDxtKey imposta le proprietà per la transizione della chiave. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione della chiave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interfaccia IDxtKey (qedit. h)
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
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328611"
---
# <a name="idxtkey-interface"></a>Interfaccia IDxtKey

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IDxtKey` interfaccia imposta le proprietà della transizione della [chiave](key-transition.md) .

Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione della chiave. Non è necessario che le applicazioni DES usino questa interfaccia. Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membri

L'interfaccia **IDxtKey** eredita da **IDXEffect**. **IDxtKey** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDxtKey** dispone di questi metodi.



| Metodo                                            | Descrizione                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**ottenere \_ Hue**](idxtkey-get-hue.md)               | Recupera il valore di tonalità su cui eseguire la chiave.<br/>                                    |
| [**Ottieni \_ Inverti**](idxtkey-get-invert.md)         | Recupera un valore booleano che indica se l'operazione del tasto è invertita.<br/> |
| [**ottenere il \_ tipo di**](idxtkey-get-keytype.md)       | Recupera il tipo di chiave.<br/>                                                  |
| [**Ottieni \_ luminanza**](idxtkey-get-luminance.md)   | Recupera il valore di luminanza su cui eseguire la chiave.<br/>                              |
| [**Ottieni \_ RGB**](idxtkey-get-rgb.md)               | Recupera il colore RGB su cui eseguire la chiave.<br/>                                    |
| [**Ottieni \_ somiglianza**](idxtkey-get-similarity.md) | Recupera l'intervallo di dati del colore che diventa trasparente.<br/>                 |
| [**Inserisci \_ tonalità**](idxtkey-put-hue.md)               | Specifica il valore di tonalità su cui eseguire la chiave.<br/>                                    |
| [**Inserisci \_ Inverti**](idxtkey-put-invert.md)         | Specifica se l'operazione chiave è invertita.<br/>                            |
| [**Inserisci \_ tipo di tipo**](idxtkey-put-keytype.md)       | Specifica il tipo di chiave.<br/>                                                  |
| [**\_luminanza put**](idxtkey-put-luminance.md)   | Specifica il valore di luminanza su cui eseguire la chiave.<br/>                              |
| [**Inserisci \_ RGB**](idxtkey-put-rgb.md)               | Specifica il colore RGB su cui eseguire la chiave.<br/>                                    |
| [**Inserisci \_ somiglianza**](idxtkey-put-similarity.md) | Specifica l'intervallo di dati del colore che diventa trasparente.<br/>                 |



 

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



 

 




