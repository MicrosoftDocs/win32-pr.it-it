---
description: Contiene gli elementi del descrittore della modalità per la matrice MonitorSourceModes nella classe WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Classe VideoModeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348426"
---
# <a name="videomodedescriptor-class"></a>Classe VideoModeDescriptor

La classe WMI **VideoModeDescriptorVideo** contiene elementi del descrittore della modalità per la matrice **MonitorSourceModes** nella classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) . Questi elementi includono funzionalità di monitoraggio, ad esempio frequenza di aggiornamento, caratteristiche dei pixel o dimensioni dell'immagine. La classe **VideoModeDescriptorVideo** contiene informazioni che sono un superset dei dati disponibili nei blocchi temporali stabiliti, standard e dettagliati.

## <a name="syntax"></a>Sintassi

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a>Members

La classe **VideoModeDescriptor** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **VideoModeDescriptor** dispone di queste proprietà.

<dl> <dt>

**CompositePolarityType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di polarità composita. Si tratta di una polarità degli impulsi di sincronizzazione orizzontali al di fuori della sincronizzazione verticale.



| Valore                                                                              | Significato                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polarità composita è positiva.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | La polarità composita è negativa.<br/>                                 |
| <dl> <dt>2 (0x2)</dt> </dl> | Non applicabile. Il tipo di sincronizzazione del segnale deve essere composto da una composizione digitale.<br/> |



 

</dd> <dt>

**HorizontalActivePixels**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pixel attivi orizzontalmente.

</dd> <dt>

**HorizontalBlankingPixels**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pixel vuoti orizzontalmente

</dd> <dt>

**HorizontalBorder**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bordo orizzontale.

</dd> <dt>

**HorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione dell'immagine orizzontale in millimetri (mm).

</dd> <dt>

**HorizontalPolarityType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di polarità orizzontale.



| Valore                                                                              | Significato                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polarità orizzontale è positiva.<br/>                               |
| <dl> <dt>1 (0x1)</dt> </dl> | La polarità orizzontale è negativa.<br/>                               |
| <dl> <dt>2 (0x2)</dt> </dl> | Non applicabile. Il tipo di sincronizzazione del segnale deve essere digitale separato.<br/> |



 

</dd> <dt>

**HorizontalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Denominatore frequenza di aggiornamento orizzontale.

</dd> <dt>

**HorizontalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numeratore della frequenza di aggiornamento orizzontale in Hertz (Hz).

</dd> <dt>

**HorizontalSyncOffset**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Offset della sincronizzazione orizzontale.

</dd> <dt>

**HorizontalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza impulso della sincronizzazione orizzontale.

</dd> <dt>

**IsInterlaced**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la modalità di visualizzazione è interlacciata.

</dd> <dt>

**IsSerrationRequired**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tipo di seghettazione obbligatorio, se appropriato.



| Valore                                                                              | Significato                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Il controller deve fornire la sincronizzazione orizzontale durante la sincronizzazione verticale.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Il controller non deve fornire la sincronizzazione orizzontale durante la sincronizzazione verticale.<br/>                             |
| <dl> <dt>2 (0x2)</dt> </dl> | Non applicabile. Il tipo di sincronizzazione del segnale deve essere bipolare, composito analogico o composito digitale.<br/> |



 

</dd> <dt>

**IsSyncOnRGB**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica quali righe del segnale video devono essere sincronizzate, se appropriato.



| Valore                                                                              | Significato                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | L'impulso di sincronizzazione dovrebbe essere visualizzato in tutte e 3 le linee del segnale video.<br/>                  |
| <dl> <dt>1 (0x1)</dt> </dl> | L'impulso di sincronizzazione dovrebbe essere visualizzato solo sulla linea del segnale video verde.<br/>          |
| <dl> <dt>2 (0x2)</dt> </dl> | Non applicabile. Il tipo di sincronizzazione del segnale deve essere composito analogico bipolare.<br/> |



 

</dd> <dt>

**PixelClockRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Frequenza di clock in pixel in Hertz (Hz).

</dd> <dt>

**StereoModeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di modalità stereo. Nella tabella seguente sono elencati i valori possibili.



| Valore                                                                              | Significato                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Nessun stereo.<br/>                                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Campo stereo sequenziale con immagine a destra nella sincronizzazione stereo.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Campo stereo sequenziale con immagine a sinistra in sincronizzazione stereo.<br/>  |
| <dl> <dt>3 (0x3)</dt> </dl> | Stereo Interleaved a 2 vie con immagine corretta su righe pari.<br/> |
| <dl> <dt>4 (0x4)</dt> </dl> | Stereo a 2 vie con interfoliazione con immagine a sinistra in linee pari.<br/>  |
| <dl> <dt>5 (0x5)</dt> </dl> | Stereo con interfoliazione a 4 vie.<br/>                                |
| <dl> <dt>6 (0x6)</dt> </dl> | Stereo con interfoliazione affiancati.<br/>                         |



 

</dd> <dt>

**SyncSignalType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di sincronizzazione segnale. Nella tabella seguente sono elencati i valori possibili.



| Valore                                                                              | Significato                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Composito analogico<br/>         |
| <dl> <dt>1 (0x1)</dt> </dl> | Composite analogico bipolare<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Composizione digitale<br/>        |
| <dl> <dt>3 (0x3)</dt> </dl> | Separato digitale<br/>         |



 

</dd> <dt>

**VerticalActivePixels**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pixel attivi verticalmente.

</dd> <dt>

**VerticalBlankingPixels**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pixel vuoti verticali.

</dd> <dt>

**VerticalBorder**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bordo verticale.

</dd> <dt>

**VerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni verticali dell'immagine in millimetri (mm).

</dd> <dt>

**VerticalPolarityType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di polarità verticale.



| Valore                                                                              | Significato                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polarità verticale è positiva.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | La polarità verticale è negativa<br/>                                  |
| <dl> <dt>2 (0x2)</dt> </dl> | Non applicabile. Il tipo di sincronizzazione del segnale deve essere digitale separato.<br/> |



 

</dd> <dt>

**VerticalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Denominatore frequenza di aggiornamento verticale.

</dd> <dt>

**VerticalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numeratore della frequenza di aggiornamento verticale in Hertz (Hz).

</dd> <dt>

**VerticalSyncOffset**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Offset sincronizzazione verticale.

</dd> <dt>

**VerticalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza impulso della sincronizzazione verticale.

</dd> <dt>

VideoStandardType
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di video standard.



| Valore                                                                                | Significato                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Altro<br/>                                                                                               |
| <dl> <dt>1 (0x1)</dt> </dl>   | VESA DMT. Da video Electronics Standard Association (VESA) display monitor Times Specification.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>   | GTF VESA. Dallo standard delle formule per la temporizzazione VESA generalizzata.<br/>                                            |
| <dl> <dt>3 (0x3)</dt> </dl>   | Standard VESA CVT/da VESA Coordinated video Times standard.<br/>                                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5)</dt> </dl>   | APPLE<br/>                                                                                               |
| <dl> <dt>6 (0x6)</dt> </dl>   | NTSC M<br/>                                                                                              |
| <dl> <dt>7 (0x7)</dt> </dl>   | NTSC J<br/>                                                                                              |
| <dl> <dt>8 (0x8)</dt> </dl>   | NTSC 433<br/>                                                                                            |
| <dl> <dt>9 (0x9)</dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xA)</dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB)</dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xC)</dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD)</dt> </dl>  | ELENCO DI ACCESSO ALLA PUBBLICAZIONE<br/>                                                                                               |
| <dl> <dt>14 (0xE)</dt> </dl>  | PAL D<br/>                                                                                               |
| <dl> <dt>15 (0xF)</dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10)</dt> </dl> | NC PAL<br/>                                                                                              |
| <dl> <dt>17 (0x11)</dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12)</dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13)</dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14)</dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15)</dt> </dl> | SECAM K<br/>                                                                                             |
| <dl> <dt>22 (0x16)</dt> </dl> | SECAM K1<br/>                                                                                            |
| <dl> <dt>23 (0x17)</dt> </dl> | SECAM L<br/>                                                                                             |
| <dl> <dt>24 (0x18)</dt> </dl> | SECAM L1<br/>                                                                                            |
| <dl> <dt>25 (0x19)</dt> </dl> | EIA861<br/>                                                                                              |
| <dl> <dt>26 (0x1A)</dt> </dl> | EIA861A<br/>                                                                                             |
| <dl> <dt>27 (0x1B)</dt> </dl> | EIA861B<br/>                                                                                             |



 

</dd> </dl>

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

 

 




