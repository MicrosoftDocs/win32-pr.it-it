---
description: L'interfaccia IDxtJpeg imposta le proprietà della transizione di cancellazione SMPTE. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione di cancellazione SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interfaccia IDxtJpeg (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326923"
---
# <a name="idxtjpeg-interface"></a>Interfaccia IDxtJpeg

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IDxtJpeg` interfaccia imposta le proprietà della transizione di [cancellazione SMPTE](smpte-wipe-transition.md) .

Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione di cancellazione SMPTE. Non è necessario che le applicazioni DES usino questa interfaccia. Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membri

L'interfaccia **IDxtJpeg** eredita da **IDXEffect**. **IDxtJpeg** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDxtJpeg** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges**](idxtjpeg-applychanges.md)              | Applica le proprietà che sono state modificate.<br/>                                      |
| [**ottenere \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Recupera il colore del bordo intorno ai bordi del pattern di cancellazione.<br/>        |
| [**ottenere \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Recupera la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.<br/> |
| [**ottenere \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Recupera la larghezza del bordo solido lungo i bordi del pattern di cancellazione.<br/>   |
| [**Ottieni \_ maskName**](idxtjpeg-get-maskname.md)             | Recupera il nome di un file JPEG da utilizzare come maschera di cancellazione.<br/>                 |
| [**ottenere \_ MaskNum**](idxtjpeg-get-masknum.md)               | Recupera il codice di cancellazione SMPTE della cancellazione.<br/>                                     |
| [**ottenere \_ offsetX**](idxtjpeg-get-offsetx.md)               | Recupera l'offset orizzontale dell'origine della cancellazione.<br/>                            |
| [**Ottieni \_ offset**](idxtjpeg-get-offsety.md)               | Recupera l'offset verticale dell'origine della cancellazione.<br/>                              |
| [**ottenere \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Recupera il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.<br/>     |
| [**ottenere la \_ replica**](idxtjpeg-get-replicatey.md)         | Recupera il numero di volte in cui il modello di cancellazione viene replicato verticalmente.<br/>       |
| [**Ottieni \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Recupera il valore in base al quale la cancellazione viene allungata orizzontalmente.<br/>              |
| [**Ottieni \_ scalabilità**](idxtjpeg-get-scaley.md)                 | Recupera il valore in base al quale la cancellazione viene allungata verticalmente.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Ripristina le impostazioni predefinite della transizione di cancellazione.<br/>                          |
| [**Inserisci \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Specifica il colore del bordo intorno ai bordi del pattern di cancellazione.<br/>        |
| [**Inserisci \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Specifica la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.<br/> |
| [**Inserisci \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Specifica lo spessore del bordo a tinta unita lungo i bordi del pattern di cancellazione.<br/>   |
| [**Inserisci \_ maskName**](idxtjpeg-put-maskname.md)             | Specifica il nome di un file JPEG da usare come maschera di cancellazione.<br/>                     |
| [**Inserisci \_ MaskNum**](idxtjpeg-put-masknum.md)               | Specifica il codice di cancellazione SMPTE della cancellazione.<br/>                                     |
| [**Inserisci \_ offsetX**](idxtjpeg-put-offsetx.md)               | Specifica l'offset orizzontale dell'origine della cancellazione.<br/>                            |
| [**Inserisci \_ offset**](idxtjpeg-put-offsety.md)               | Specifica l'offset verticale dell'origine della cancellazione.<br/>                              |
| [**Inserisci \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Specifica il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.<br/>     |
| [**Inserisci \_ replica**](idxtjpeg-put-replicatey.md)         | Specifica il numero di volte in cui il modello di cancellazione viene replicato verticalmente.<br/>       |
| [**Inserisci \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Specifica la quantità in base alla quale la cancellazione viene allungata orizzontalmente.<br/>              |
| [**\_scalabilità orizzontale**](idxtjpeg-put-scaley.md)                 | Specifica la quantità in base alla quale la cancellazione viene allungata verticalmente.<br/>                |



 

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



 

 




