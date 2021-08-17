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
ms.openlocfilehash: 958eb9134062d5380a2afda77eeaad3034a2da7430d2f6a3094916ceae211e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926783"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Classe WmiMonitorBasicDisplayParams

La **classe WMI WmiMonitorBasicDisplayParams** rappresenta le funzionalità di visualizzazione di base di un monitor del computer. Il valore della proprietà **VideoInputType** indica se il monitor è analogico o digitale. I dati in questa classe corrispondono ai dati nel blocco Basic Display Parameters/Features dello standard VESA (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID).

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

La **classe WmiMonitorBasicDisplayParams** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WmiMonitorBasicDisplayParams** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Caratteristica di trasferimento dello schermo (100 \* Gamma-100).

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni massime dell'immagine orizzontale in centimetri. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
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

Visualizzare le funzionalità supportate dal monitoraggio.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
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

**MaxHorizontalImageSize** e **MaxVerticalImageSize** rappresentano le dimensioni massime dell'immagine che il monitor può visualizzare correttamente per l'intero set di combinazioni di temporizzazione e formato supportate. La dimensione massima dell'immagine è definita dallo standard VIAD (Video Image Area Definition) VESA e viene arrotondata al centimetro più vicino. Il computer host può usare questi dati per selezionare le dimensioni e le proporzioni dell'immagine che consentiranno il ridimensionamento corretto del testo. Tenere presente che, se uno o entrambi questi campi sono pari a zero, il sistema non fa ipotesi sulle dimensioni di visualizzazione. Ad esempio, le dimensioni di una visualizzazione di proiezione possono essere indeterminate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




