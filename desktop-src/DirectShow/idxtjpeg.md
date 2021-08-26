---
description: L'interfaccia IDxtJpeg imposta le proprietà per la transizione di cancellazione SMPTE. Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering della transizione di cancellazione SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interfaccia IDxtJpeg (Qedit.h)
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
ms.openlocfilehash: b1f48ff04c087c0c0c391eaf1a64ae8e7768505a5ba8d108ab49c54ffc7b17f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997501"
---
# <a name="idxtjpeg-interface"></a>Interfaccia IDxtJpeg

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`IDxtJpeg`L'interfaccia imposta le proprietà nella transizione di [cancellazione SMPTE.](smpte-wipe-transition.md)

Questa interfaccia viene usata internamente da DirectShow Editing Services (DES) quando esegue il rendering della transizione di cancellazione SMPTE. Le applicazioni DES non devono usare questa interfaccia. Per impostare le proprietà in una transizione in DES, usare [**l'interfaccia IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Membri

**L'interfaccia IDxtJpeg** eredita da **IDXEffect**. **IDxtJpeg** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IDxtJpeg.**



| Metodo                                                     | Descrizione                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Applychanges**](idxtjpeg-applychanges.md)              | Applica tutte le proprietà modificate.<br/>                                      |
| [**get \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Recupera il colore del bordo intorno ai bordi del modello di cancellazione.<br/>        |
| [**ottenere \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Recupera la larghezza dell'area sfocata intorno ai bordi del modello di cancellazione.<br/> |
| [**get \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Recupera la larghezza del bordo a tinta unita lungo i bordi del modello di cancellazione.<br/>   |
| [**get \_ MaskName**](idxtjpeg-get-maskname.md)             | Recupera il nome di un file JPEG da usare come maschera di cancellazione.<br/>                 |
| [**get \_ MaskNum**](idxtjpeg-get-masknum.md)               | Recupera il codice di cancellazione SMPTE della cancellazione.<br/>                                     |
| [**get \_ OffsetX**](idxtjpeg-get-offsetx.md)               | Recupera l'offset orizzontale dell'origine di cancellazione.<br/>                            |
| [**get \_ OffsetY**](idxtjpeg-get-offsety.md)               | Recupera l'offset verticale dell'origine di cancellazione.<br/>                              |
| [**ottenere \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Recupera il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.<br/>     |
| [**get \_ ReplicateY**](idxtjpeg-get-replicatey.md)         | Recupera il numero di volte in cui il modello di cancellazione viene replicato verticalmente.<br/>       |
| [**ottenere \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Recupera la quantità di estensione orizzontale della cancellazione.<br/>              |
| [**ottenere \_ ScaleY**](idxtjpeg-get-scaley.md)                 | Recupera la quantità di estensione verticale della cancellazione.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Ripristina le impostazioni predefinite della transizione Cancellazione dati.<br/>                          |
| [**put \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Specifica il colore del bordo intorno ai bordi del modello di cancellazione.<br/>        |
| [**put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Specifica la larghezza dell'area sfocata intorno ai bordi del modello di cancellazione.<br/> |
| [**put \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Specifica la larghezza del bordo a tinta unita lungo i bordi del modello di cancellazione.<br/>   |
| [**put \_ MaskName**](idxtjpeg-put-maskname.md)             | Specifica il nome di un file JPEG da usare come maschera di cancellazione.<br/>                     |
| [**put \_ MaskNum**](idxtjpeg-put-masknum.md)               | Specifica il codice di cancellazione SMPTE della cancellazione.<br/>                                     |
| [**put \_ OffsetX**](idxtjpeg-put-offsetx.md)               | Specifica l'offset orizzontale dell'origine di cancellazione.<br/>                            |
| [**put \_ OffsetY**](idxtjpeg-put-offsety.md)               | Specifica l'offset verticale dell'origine di cancellazione.<br/>                              |
| [**put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Specifica il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.<br/>     |
| [**put \_ ReplicateY**](idxtjpeg-put-replicatey.md)         | Specifica il numero di volte in cui il modello di cancellazione viene replicato verticalmente.<br/>       |
| [**put \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Specifica la quantità di estensione orizzontale della cancellazione.<br/>              |
| [**put \_ ScaleY**](idxtjpeg-put-scaley.md)                 | Specifica la quantità di estensione verticale della cancellazione.<br/>                |



 

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



 

 




