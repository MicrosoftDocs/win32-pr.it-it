---
description: Rappresenta le funzionalità di visualizzazione di base di un monitor del computer.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Classe WmiMonitorBasicDisplayParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315744"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Classe WmiMonitorBasicDisplayParams

La classe WMI **WmiMonitorBasicDisplayParams** rappresenta le funzionalità di visualizzazione di base di un monitor computer. Il valore della proprietà **VideoInputType** indica se il monitoraggio è analogico o digitale. I dati in questa classe corrispondono ai dati nel blocco Basic display Parameters/features di video Electronics Standard Association (VESA) Enhanced Extended Display Data (E-EDID) standard.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a>Members

La classe **WmiMonitorBasicDisplayParams** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WmiMonitorBasicDisplayParams** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Caratteristica di trasferimento di visualizzazione (100 \* gamma-100).

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni massime dell'immagine orizzontale in centimetri. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni massime dell'immagine verticale in centimetri. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Visualizza le funzionalità supportate dal monitoraggio.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di input video.



| Valore                                                                              | Significato            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analogico<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digitale<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

**MaxHorizontalImageSize** e **MaxVerticalImageSize** rappresentano le dimensioni massime dell'immagine che il monitoraggio è in grado di visualizzare correttamente per l'intero set di combinazioni di formato e temporizzazione supportate. La dimensione massima dell'immagine è definita dallo standard VIAD (video image area Definition) VESA ed è arrotondata al centimetro più vicino. Il computer host può usare questi dati per selezionare le dimensioni e le proporzioni dell'immagine che consentiranno il testo ridimensionato correttamente. Tenere presente che, se uno o entrambi i campi sono pari a zero, il sistema non prevede alcuna supposizione sulle dimensioni di visualizzazione. Ad esempio, le dimensioni di una visualizzazione di proiezione potrebbero non essere determinate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




