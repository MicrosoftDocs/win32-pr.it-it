---
description: Nell'elenco seguente vengono fornite le descrizioni degli elementi della proprietà supportati da Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descrizioni degli elementi delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636123"
---
# <a name="property-item-descriptions"></a>Descrizioni degli elementi delle proprietà

Nell'elenco seguente vengono fornite le descrizioni degli elementi della proprietà supportati da Windows GDI+. Le descrizioni sono brevi e generali in modo da essere valide per un'ampia gamma di formati di file di immagine. Per una descrizione dettagliata del modo in cui un elemento di proprietà viene usato da un particolare formato di file, vedere la specifica del formato di file. Per i collegamenti a diverse specifiche di file e ad altri documenti che descrivono i metadati in dettaglio, vedere [specifiche del formato del file di immagine](-gdiplus-constant-image-file-format-specifications.md).

Il formato EXIF (Exchangeable image file) è uno standard JEIDA (Japan Electronic Industry Development Association), modificato il 1998 giugno come versione 2,1. Le parti della specifica EXIF vengono usate con l'autorizzazione di JEIDA.

## <a name="propertytaggpsver"></a>PropertyTagGpsVer

Versione di Global Positioning Systems (GPS) IFD, specificata come 2.0.0.0. Questo tag è obbligatorio quando è presente il tag PropertyTagGpsIFD. Quando la versione è 2.0.0.0, il valore del tag è 0x02000000.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0000              |
| Tipo  | PropertyTagTypeByte |
| Conteggio | 4                   |



 

## <a name="propertytaggpslatituderef"></a>PropertyTagGpsLatitudeRef

Stringa di caratteri con terminazione null che specifica se la latitudine è nord o sud. `N` Specifica la latitudine nord e `S` specifica la latitudine sud.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0001                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpslatitude"></a>PropertyTagGpsLatitude

Latitudine. La latitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi. Quando vengono espressi i gradi, i minuti e i secondi, il formato è gg/1, mm/1, SS/1. Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DD/1, mmmm/100, 0/1.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0002                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytaggpslongituderef"></a>PropertyTagGpsLongitudeRef

Stringa di caratteri con terminazione null che specifica se la longitudine è la longitudine est o ovest. `E` Specifica la longitudine est e `W` specifica la longitudine ovest.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0003                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpslongitude"></a>PropertyTagGpsLongitude

Longitudine. La longitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi. Quando vengono espressi i gradi, i minuti e i secondi, il formato è DDD/1, mm/1, SS/1. Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DDD/1, mmmm/100, 0/1.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0004                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytaggpsaltituderef"></a>PropertyTagGpsAltitudeRef

Altitudine di riferimento, in metri.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0005              |
| Tipo  | PropertyTagTypeByte |
| Conteggio | 1                   |



 

## <a name="propertytaggpsaltitude"></a>PropertyTagGpsAltitude

Altitudine, in metri, basata sull'altitudine di riferimento specificata da PropertyTagGpsAltitudeRef.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0006                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaggpsgpstime"></a>PropertyTagGpsGpsTime

Ora UTC (Coordinated Universal Time). Il valore viene espresso come tre numeri razionali che forniscono l'ora, il minuto e il secondo.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0007                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytaggpsgpssatellites"></a>PropertyTagGpsGpsSatellites

Stringa di caratteri con terminazione null che specifica i satelliti GPS usati per le misurazioni. Questo tag può essere usato per specificare il numero di ID, l'angolo di elevazione, Azimut, SNR e altre informazioni su ogni satellite. Il formato non è specificato. Se il ricevitore GPS non è in grado di eseguire misure, il valore del tag deve essere impostato su **null**.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0008                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytaggpsgpsstatus"></a>PropertyTagGpsGpsStatus

Stringa di caratteri con terminazione null che specifica lo stato del ricevitore GPS quando l'immagine viene registrata. `A` indica che la misurazione è in corso e `V` indica che la misura è interoperabilità.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0009                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsgpsmeasuremode"></a>PropertyTagGpsGpsMeasureMode

Stringa di caratteri con terminazione null che specifica la modalità di misurazione GPS. `2` Specifica la misurazione 2D e specifica la `3` misurazione 3D.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x000A                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsgpsdop"></a>PropertyTagGpsGpsDop

DOP GPS (grado di precisione dei dati). Un valore HDOP viene scritto durante la misurazione 2D e viene scritto un valore PDOP durante la misurazione 3D.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x000B                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaggpsspeedref"></a>PropertyTagGpsSpeedRef

Stringa di caratteri con terminazione null che specifica l'unità utilizzata per esprimere la velocità di spostamento del ricevitore GPS. `K`, `M` e `N` rappresentano rispettivamente i chilometri all'ora, le miglia all'ora e i nodi.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x000C                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsspeed"></a>PropertyTagGpsSpeed

Velocità di spostamento del ricevitore GPS.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x000D                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaggpstrackref"></a>PropertyTagGpsTrackRef

Stringa di caratteri con terminazione null che specifica il riferimento per fornire la direzione dello spostamento del ricevitore GPS. `T` Specifica la direzione vera e `M` specifica la direzione magnetica.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x000E                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpstrack"></a>PropertyTagGpsTrack

Direzione dello spostamento del ricevitore GPS. L'intervallo di valori è compreso tra 0,00 e 359,99.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x000F                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaggpsimgdirref"></a>PropertyTagGpsImgDirRef

Stringa di caratteri con terminazione null che specifica il riferimento per la direzione dell'immagine quando viene acquisita. `T` Specifica la direzione vera e `M` specifica la direzione magnetica.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0010                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsimgdir"></a>PropertyTagGpsImgDir

Direzione dell'immagine al momento dell'acquisizione. L'intervallo di valori è compreso tra 0,00 e 359,99.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0011                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaggpsmapdatum"></a>PropertyTagGpsMapDatum

Stringa di caratteri con terminazione null che specifica i dati del sondaggio geodetici utilizzati dal ricevitore GPS. Se i dati del sondaggio sono limitati al Giappone, il valore di questo tag è `TOKYO` o `WGS-84` .



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0012                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytaggpsdestlatref"></a>PropertyTagGpsDestLatRef

Stringa di caratteri con terminazione null che specifica se la latitudine del punto di destinazione è la latitudine nord o sud. `N` Specifica la latitudine nord e `S` specifica la latitudine sud.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0013                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsdestlat"></a>PropertyTagGpsDestLat

Latitudine del punto di destinazione. La latitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi. Quando vengono espressi i gradi, i minuti e i secondi, il formato è gg/1, mm/1, SS/1. Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DD/1, mmmm/100, 0/1.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0014                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytaggpsdestlongref"></a>PropertyTagGpsDestLongRef

Stringa di caratteri con terminazione null che specifica se la longitudine del punto di destinazione è la longitudine est o ovest. `E` Specifica la longitudine est e `W` specifica la longitudine ovest.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0015                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsdestlong"></a>PropertyTagGpsDestLong

Longitudine del punto di destinazione. La longitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi. Quando vengono espressi i gradi, i minuti e i secondi, il formato è DDD/1, mm/1, SS/1. Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DDD/1, mmmm/100, 0/1.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0016                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytaggpsdestbearref"></a>PropertyTagGpsDestBearRef

Stringa di caratteri con terminazione null che specifica il riferimento usato per assegnare il cuscinetto al punto di destinazione. `T` Specifica la direzione vera e `M` specifica la direzione magnetica.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0017                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsdestbear"></a>PropertyTagGpsDestBear

Che comportano il punto di destinazione. L'intervallo di valori è compreso tra 0,00 e 359,99.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0018                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaggpsdestdistref"></a>PropertyTagGpsDestDistRef

Stringa di caratteri con terminazione null che specifica l'unità utilizzata per esprimere la distanza al punto di destinazione. K, M e N rappresentano rispettivamente i chilometri, le miglia e i nodi.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------------------------|
| Tag   | 0x0019                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Conteggio | 2 (un carattere più il carattere di terminazione NULL) |



 

## <a name="propertytaggpsdestdist"></a>PropertyTagGpsDestDist

Distanza al punto di destinazione.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x001A                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagnewsubfiletype"></a>PropertyTagNewSubfileType

Tipo di dati in un file di dati.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x00FE              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagsubfiletype"></a>PropertyTagSubfileType

Tipo di dati in un file di dati.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x00FF               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagimagewidth"></a>PropertyTagImageWidth

Numero di pixel per riga.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0100                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagimageheight"></a>PropertyTagImageHeight

Numero di righe in pixel.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0101                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagbitspersample"></a>PropertyTagBitsPerSample

Numero di bit per componente colore. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0102                                   |
| Tipo  | PropertyTagTypeShort                     |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagcompression"></a>PropertyTagCompression

Schema di compressione usato per i dati dell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0103               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagphotometricinterp"></a>PropertyTagPhotometricInterp

Come verranno interpretati i dati pixel.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0106               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthreshholding"></a>PropertyTagThreshHolding

Tecnica utilizzata per eseguire la conversione da pixel grigi a pixel neri e bianchi.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0107               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagcellwidth"></a>PropertyTagCellWidth

Larghezza della matrice di retinatura o di mezzitoni.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0108               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagcellheight"></a>PropertyTagCellHeight

Altezza della matrice di retinatura o di mezzitoni.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0109               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagfillorder"></a>PropertyTagFillOrder

Ordine logico dei bit in un byte.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x010A               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagdocumentname"></a>PropertyTagDocumentName

Stringa di caratteri con terminazione null che specifica il nome del documento da cui è stata analizzata l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x010D                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagimagedescription"></a>PropertyTagImageDescription

Stringa di caratteri con terminazione null che specifica il titolo dell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x010E                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagequipmake"></a>PropertyTagEquipMake

Stringa di caratteri con terminazione null che specifica il produttore dell'apparecchiatura utilizzata per registrare l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x010F                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagequipmodel"></a>PropertyTagEquipModel

Stringa di caratteri con terminazione null che specifica il nome del modello o il numero di modello dell'apparecchiatura utilizzata per registrare l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0110                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagstripoffsets"></a>PropertyTagStripOffsets

Per ogni striscia, l'offset dei byte di tale striscia. Vedere anche [PropertyTagRowsPerStrip](#propertytagrowsperstrip) e [PropertyTagStripBytesCount](#propertytagstripbytescount).



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0111                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | Numero di strisce                            |



 

## <a name="propertytagorientation"></a>PropertyTagOrientation

Orientamento dell'immagine visualizzato in termini di righe e colonne.



Tag

0x0112

Tipo

PropertyTagTypeShort

Conteggio

1

1-la riga 0A si trova nella parte superiore dell'immagine visiva e la colonna 0A è il lato sinistro dell'oggetto visivo. 2-la riga 0A si trova nella parte superiore dell'immagine e la colonna 0A è il lato destro dell'oggetto visivo. 3-la riga 0A si trova nella parte inferiore dell'immagine e la colonna 0A è il lato destro dell'oggetto visivo. 4-la riga 0A si trova nella parte inferiore dell'immagine e la colonna 0A è il lato sinistro dell'oggetto visivo. 5-la riga 0A è il lato sinistro dell'immagine e la colonna 0A è la parte superiore dell'oggetto visivo. 6: la riga 0A è il lato visivo destro dell'immagine e la colonna 0A è la parte superiore dell'oggetto visivo. 7-la riga 0A è il lato visivo destro dell'immagine e la colonna 0A è la parte inferiore dell'oggetto visivo. 8: la riga 0A è il lato sinistro dell'immagine e la colonna 0A è la parte inferiore dell'oggetto visivo.



 

## <a name="propertytagsamplesperpixel"></a>PropertyTagSamplesPerPixel

Numero di componenti colore per pixel.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0115               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagrowsperstrip"></a>PropertyTagRowsPerStrip

Numero di righe per striscia. Vedere anche [PropertyTagStripBytesCount](#propertytagstripbytescount) e [PropertyTagStripOffsets](#propertytagstripoffsets).



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0116                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagstripbytescount"></a>PropertyTagStripBytesCount

Per ogni striscia, il numero totale di byte in tale striping.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0117                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | Numero di strisce                            |



 

## <a name="propertytagminsamplevalue"></a>PropertyTagMinSampleValue

Per ogni componente del colore, valore minimo assegnato a tale componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0118                                   |
| Tipo  | PropertyTagTypeShort                     |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagmaxsamplevalue"></a>PropertyTagMaxSampleValue

Per ogni componente del colore, valore massimo assegnato a tale componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0119                                   |
| Tipo  | PropertyTagTypeShort                     |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagxresolution"></a>PropertyTagXResolution

Numero di pixel per unità nella direzione della larghezza dell'immagine (x). L'unità è specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x011A                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagyresolution"></a>PropertyTagYResolution

Numero di pixel per unità nella direzione altezza (y) immagine. L'unità è specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x011B                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagplanarconfig"></a>PropertyTagPlanarConfig

Indica se i componenti pixel sono registrati in formato a più grossi o planari.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x011C               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagpagename"></a>PropertyTagPageName

Stringa di caratteri con terminazione null che specifica il nome della pagina da cui è stata analizzata l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x011D                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagxposition"></a>PropertyTagXPosition

Offset dal lato sinistro della pagina al lato sinistro dell'immagine. L'unità di misura viene specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x011E                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagyposition"></a>PropertyTagYPosition

Offset dalla parte superiore della pagina alla parte superiore dell'immagine. L'unità di misura viene specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x011F                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagfreeoffset"></a>PropertyTagFreeOffset

Per ogni stringa di byte contigui non utilizzati, offset di byte di tale stringa.



| Informazioni sulle proprietà | Valore |
|------|---------------------|
| Tag  | 0x0120              |
| Tipo | PropertyTagTypeLong |



 

## <a name="propertytagfreebytecounts"></a>PropertyTagFreeByteCounts

Per ogni stringa di byte contigui non utilizzati, numero di byte in tale stringa.



| Informazioni sulle proprietà | Valore |
|-------|-----------------------------------------------|
| Tag   | 0x0121                                        |
| Tipo  | PropertyTagTypeLong                           |
| Conteggio | Numero di stringhe di byte contigui non utilizzati. |



 

## <a name="propertytaggrayresponseunit"></a>PropertyTagGrayResponseUnit

Precisione del numero specificato da PropertyTagGrayResponseCurve. 1 specifica i decimi, 2 specifica i centesimi, 3 specifica i millesimi e così via.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0122               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytaggrayresponsecurve"></a>PropertyTagGrayResponseCurve

Per ogni possibile valore in pixel in un'immagine in scala di grigi, la densità ottica del valore del pixel.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------|
| Tag   | 0x0123                          |
| Tipo  | PropertyTagTypeShort            |
| Conteggio | Numero di possibili valori pixel |



 

## <a name="propertytagt4option"></a>PropertyTagT4Option

Set di flag correlati alla codifica T4.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0124              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagt6option"></a>PropertyTagT6Option

Set di flag correlati alla codifica T6.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0125              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagresolutionunit"></a>PropertyTagResolutionUnit

Unità di misura per la risoluzione orizzontale e la risoluzione verticale.



Tag

0x0128

Tipo

PropertyTagTypeShort

Conteggio

1

2-pollice 3 centimetri



 

## <a name="propertytagpagenumber"></a>PropertyTagPageNumber

Numero di pagina della pagina da cui è stata analizzata l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0129               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagtransferfunction"></a>PropertyTagTransferFunction

Tabelle che specificano le funzioni di trasferimento per l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------------------|
| Tag   | 0x012D                                               |
| Tipo  | PropertyTagTypeShort                                 |
| Conteggio | Numero totale di parole a 16 bit necessarie per le tabelle |



 

## <a name="propertytagsoftwareused"></a>PropertyTagSoftwareUsed

Stringa di caratteri con terminazione null che specifica il nome e la versione del software o del firmware del dispositivo usato per generare l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0131                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagdatetime"></a>PropertyTagDateTime

Data e ora di creazione dell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0132               |
| Tipo  | PropertyTagTypeASCII |
| Conteggio | 20                   |



 

## <a name="propertytagartist"></a>PropertyTagArtist

Stringa di caratteri con terminazione null che specifica il nome della persona che ha creato l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x013B                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytaghostcomputer"></a>PropertyTagHostComputer

Stringa di caratteri con terminazione null che specifica il computer e/o il sistema operativo utilizzato per creare l'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x013C                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagpredictor"></a>PropertyTagPredictor

Tipo di schema di stima applicato ai dati dell'immagine prima dell'applicazione dello schema di codifica.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x013D               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagwhitepoint"></a>PropertyTagWhitePoint

Cromaticità del punto bianco dell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x013E                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 2                       |



 

## <a name="propertytagprimarychromaticities"></a>PropertyTagPrimaryChromaticities

Per ognuno dei tre colori primari nell'immagine, la cromaticità di tale colore.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x013F                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 6                       |



 

## <a name="propertytagcolormap"></a>PropertyTagColorMap

Tavolozza dei colori (tabella di ricerca) per un'immagine con indicizzazione della tavolozza.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------------------------------|
| Tag   | 0x0140                                          |
| Tipo  | PropertyTagTypeShort                            |
| Conteggio | Numero di parole a 16 bit richieste per la tavolozza |



 

## <a name="propertytaghalftonehints"></a>PropertyTagHalftoneHints

Informazioni usate dalla funzione mezzitoni



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0141               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 2                    |



 

## <a name="propertytagtilewidth"></a>PropertyTagTileWidth

Numero di colonne in pixel in ogni sezione.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0142                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagtilelength"></a>PropertyTagTileLength

Numero di righe in pixel in ogni sezione.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0143                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagtileoffset"></a>PropertyTagTileOffset

Per ogni sezione, l'offset dei byte di tale riquadro.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0144              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | Numero di riquadri     |



 

## <a name="propertytagtilebytecounts"></a>PropertyTagTileByteCounts

Per ogni riquadro, il numero di byte in tale riquadro.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0145                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | Numero di riquadri                             |



 

## <a name="propertytaginkset"></a>PropertyTagInkSet

Set di inchiostri utilizzati in un'immagine separata.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x014C               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytaginknames"></a>PropertyTagInkNames

Sequenza di stringhe di caratteri concatenate con terminazione null che specificano i nomi degli inchiostri utilizzati in un'immagine separata.



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------------------------------------|
| Tag   | 0x014D                                                                 |
| Tipo  | PropertyTagTypeASCII                                                   |
| Conteggio | Lunghezza totale della sequenza di stringhe, inclusi i caratteri di terminazione NULL |



 

## <a name="propertytagnumberofinks"></a>PropertyTagNumberOfInks

Numero di inchiostri.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x014E               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagdotrange"></a>PropertyTagDotRange

Valori dei componenti colore che corrispondono a un punto 0% e a un punto 100%.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x0150                                      |
| Tipo  | PropertyTagTypeByte o PropertyTagTypeShort |
| Conteggio | 2 o 2 × PropertyTagSamplesPerPixel           |



 

## <a name="propertytagtargetprinter"></a>PropertyTagTargetPrinter

Stringa di caratteri con terminazione null che descrive l'ambiente di stampa previsto.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0151                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagextrasamples"></a>PropertyTagExtraSamples

Numero di componenti dei colori aggiuntivi. Ad esempio, un componente aggiuntivo potrebbe avere un valore alfa.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0152               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagsampleformat"></a>PropertyTagSampleFormat

Per ogni componente del colore, formato numerico (senza segno, firmato, a virgola mobile) del componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0153                                   |
| Tipo  | PropertyTagTypeShort                     |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagsminsamplevalue"></a>PropertyTagSMinSampleValue

Per ogni componente del colore, valore minimo di tale componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|-----------------------------------------------------|
| Tag   | 0x0154                                              |
| Tipo  | Il tipo più adatto ai dati del componente pixel |
| Conteggio | Numero di campioni (componenti) per pixel            |



 

## <a name="propertytagsmaxsamplevalue"></a>PropertyTagSMaxSampleValue

Per ogni componente del colore, valore massimo di tale componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|-----------------------------------------------------|
| Tag   | 0x0155                                              |
| Tipo  | Il tipo più adatto ai dati del componente pixel |
| Conteggio | Numero di campioni (componenti) per pixel            |



 

## <a name="propertytagtransferrange"></a>PropertyTagTransferRange

Tabella di valori che estende l'intervallo della funzione di trasferimento.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0156               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 6                    |



 

## <a name="propertytagjpegproc"></a>PropertyTagJPEGProc

Processo di compressione JPEG.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0200               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagjpeginterformat"></a>PropertyTagJPEGInterFormat

Offset all'inizio di un bitstream JPEG.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0201              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagjpeginterlength"></a>PropertyTagJPEGInterLength

Lunghezza, in byte, del file Bitstream JPEG.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x0202              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagjpegrestartinterval"></a>PropertyTagJPEGRestartInterval

Lunghezza dell'intervallo di riavvio.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0203               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagjpeglosslesspredictors"></a>PropertyTagJPEGLosslessPredictors

Per ogni componente del colore, valore di predittore senza perdita di selezione per il componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0205                                   |
| Tipo  | PropertyTagTypeShort                     |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagjpegpointtransforms"></a>PropertyTagJPEGPointTransforms

Per ogni componente del colore, un valore di trasformazione punto per tale componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0206                                   |
| Tipo  | PropertyTagTypeShort                     |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagjpegqtables"></a>PropertyTagJPEGQTables

Per ogni componente del colore, offset della tabella di quantizzazione per il componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0207                                   |
| Tipo  | PropertyTagTypeLong                      |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagjpegdctables"></a>PropertyTagJPEGDCTables

Per ogni componente del colore, l'offset della tabella di Huffman del controller di dominio (o della tabella Huffman) per quel componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0208                                   |
| Tipo  | PropertyTagTypeLong                      |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagjpegactables"></a>PropertyTagJPEGACTables

Per ogni componente del colore, l'offset alla tabella del Huffman AC per quel componente. Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------|
| Tag   | 0x0209                                   |
| Tipo  | PropertyTagTypeLong                      |
| Conteggio | Numero di campioni (componenti) per pixel |



 

## <a name="propertytagycbcrcoefficients"></a>PropertyTagYCbCrCoefficients

Coefficienti per la trasformazione da RGB a dati di immagine YCbCr.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0211                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytagycbcrsubsampling"></a>PropertyTagYCbCrSubsampling

Rapporto di campionamento dei componenti cromatura in relazione al componente luminanza.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0212               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 2                    |



 

## <a name="propertytagycbcrpositioning"></a>PropertyTagYCbCrPositioning

Posizione dei componenti cromatura in relazione al componente di luminanza.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x0213               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagrefblackwhite"></a>PropertyTagREFBlackWhite

Valore punto nero di riferimento e valore punto bianco di riferimento.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0214                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 6                       |



 

## <a name="propertytaggamma"></a>PropertyTagGamma

Valore gamma associato all'immagine. Il valore gamma viene archiviato come numero razionale (coppia di **caratteri Long**) con un numeratore di 100000. Ad esempio, un valore gamma di 2,2 viene archiviato come coppia (100000, 45455).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x0301                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagiccprofiledescriptor"></a>PropertyTagICCProfileDescriptor

Stringa di caratteri con terminazione null che identifica un profilo ICC.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0302                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagsrgbrenderingintent"></a>PropertyTagSRGBRenderingIntent

Modalità di visualizzazione dell'immagine in base a quanto definito da International Color Consortium (ICC). Se un oggetto  [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ viene costruito con il parametro *UseEmbeddedColorManagement* impostato su **true**, GDI+ esegue il rendering dell'immagine in base alla finalità di rendering specificata. Lo scopo può essere impostato su percettivo, colorimetrico relativo, saturazione o colorimetrico assoluto.

-   Finalità percettiva, ideale per le fotografie, offre un adattamento ottimale alla gamma di dispositivi di visualizzazione a scapito dell'accuratezza di colorimetrico.
-   La finalità colorimetrico relativa è adatta per le immagini (ad esempio, i loghi) che richiedono la corrispondenza dell'aspetto dei colori rispetto al punto bianco del dispositivo di visualizzazione.
-   Il livello di saturazione, adatto per grafici e grafici, conserva la saturazione a scapito di tonalità e luminosità.
-   Lo scopo di colorimetrico assoluto è adatto alle prove (anteprime delle immagini destinate a un dispositivo di visualizzazione diverso) che richiedono la conservazione dei colorimetria assoluti.



Tag

0x0303

Tipo

BYTE

Conteggio

1

0-percettivo 1: colorimetrico relativo 2-saturazione 3-colorimetrico assoluto



 

## <a name="propertytagimagetitle"></a>PropertyTagImageTitle

Stringa di caratteri con terminazione null che specifica il titolo dell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x0320                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagresolutionxunit"></a>PropertyTagResolutionXUnit

Unità in cui visualizzare la risoluzione orizzontale.



Tag

0x5001

Tipo

PropertyTagTypeShort

Conteggio

1

1-pixel per pollice 2-pixel per centimetro



 

## <a name="propertytagresolutionyunit"></a>PropertyTagResolutionYUnit

Unità in cui visualizzare la risoluzione verticale.



Tag

0x5002

Tipo

PropertyTagTypeShort

Conteggio

1

1-pixel per pollice 2-pixel per centimetro



 

## <a name="propertytagresolutionxlengthunit"></a>PropertyTagResolutionXLengthUnit

Unità in cui visualizzare la larghezza dell'immagine.



Tag

0x5003

Tipo

PropertyTagTypeShort

Conteggio

1

1-pollici 2-centimetri 3-punti 4-Pica 5-colonne



 

## <a name="propertytagresolutionylengthunit"></a>PropertyTagResolutionYLengthUnit

Unità in cui visualizzare l'altezza dell'immagine.



Tag

0x5004

Tipo

PropertyTagTypeShort

Conteggio

1

1-pollici 2-centimetri 3-punti 4-Pica 5-colonne



 

## <a name="propertytagprintflags"></a>PropertyTagPrintFlags

Sequenza di valori booleani a un byte che specificano le opzioni di stampa.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5005               |
| Tipo  | PropertyTagTypeASCII |
| Conteggio | Numero di flag      |



 

## <a name="propertytagprintflagsversion"></a>PropertyTagPrintFlagsVersion

Versione dei flag di stampa.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5006               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagprintflagscrop"></a>PropertyTagPrintFlagsCrop

Segni di ritaglio al centro di flag di stampa.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5007              |
| Tipo  | PropertyTagTypeByte |
| Conteggio | 1                   |



 

## <a name="propertytagprintflagsbleedwidth"></a>PropertyTagPrintFlagsBleedWidth

Larghezza del Bleed del flag di stampa.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5008              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a>PropertyTagPrintFlagsBleedWidthScale

Ridimensionamento della larghezza del Bleed del flag di stampa.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5009               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytaghalftonelpi"></a>PropertyTagHalftoneLPI

Frequenza dello schermo dell'input penna, in linee per pollice.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x500A                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaghalftonelpiunit"></a>PropertyTagHalftoneLPIUnit

Unità per la frequenza dello schermo.



Tag

0x500B

Tipo

PropertyTagTypeShort

Conteggio

1

1-righe per pollice 2-linee per centimetro



 

## <a name="propertytaghalftonedegree"></a>PropertyTagHalftoneDegree

Angolo per lo schermo.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x500C                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytaghalftoneshape"></a>PropertyTagHalftoneShape

Forma dei punti di mezzitoni.



Tag

0x500D

Tipo

PropertyTagTypeShort

Conteggio

1

0-Round 1-ellisse 2-line 3-Square 4-Cross 6-Diamond



 

## <a name="propertytaghalftonemisc"></a>PropertyTagHalftoneMisc

Informazioni varie su mezzitoni.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x500E              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytaghalftonescreen"></a>PropertyTagHalftoneScreen

Valore booleano che specifica se utilizzare le schermate predefinite della stampante.



Tag

0x500F

Tipo

PropertyTagTypeByte

Conteggio

1

1-utilizzare le schermate predefinite della stampante 2-altro



 

## <a name="propertytagjpegquality"></a>PropertyTagJPEGQuality

Tag privato usato dal formato Adobe Photoshop. Non per uso pubblico.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5010               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | Qualsiasi                  |



 

## <a name="propertytaggridsize"></a>PropertyTagGridSize

Blocco di informazioni su griglie e guide.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x5011                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

## <a name="propertytagthumbnailformat"></a>PropertyTagThumbnailFormat

Formato dell'immagine di anteprima.



Tag

0x5012

Tipo

PropertyTagTypeLong

Conteggio

1

0-RGB RAW 1-JPEG



 

## <a name="propertytagthumbnailwidth"></a>PropertyTagThumbnailWidth

Larghezza, in pixel, dell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5013              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagthumbnailheight"></a>PropertyTagThumbnailHeight

Altezza, in pixel, dell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5014              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagthumbnailcolordepth"></a>PropertyTagThumbnailColorDepth

bit per pixel (BPP) per l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5015               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailplanes"></a>PropertyTagThumbnailPlanes

Numero di piani di colore per l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5016               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailrawbytes"></a>PropertyTagThumbnailRawBytes

Offset dei byte tra le righe di dati pixel.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5017              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagthumbnailsize"></a>PropertyTagThumbnailSize

Dimensioni totali, in byte, dell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5018              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagthumbnailcompressedsize"></a>PropertyTagThumbnailCompressedSize

Dimensioni compresse, in byte, dell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5019              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagcolortransferfunction"></a>PropertyTagColorTransferFunction

Tabella di valori che specificano le funzioni di trasferimento dei colori.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x501A                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

## <a name="propertytagthumbnaildata"></a>PropertyTagThumbnailData

Bit di anteprima non elaborati in formato JPEG o RGB. Dipende da PropertyTagThumbnailFormat.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x501B              |
| Tipo  | PropertyTagTypeByte |
| Conteggio | Variabile            |



 

## <a name="propertytagthumbnailimagewidth"></a>PropertyTagThumbnailImageWidth

Numero di pixel per riga nell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x5020                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagthumbnailimageheight"></a>PropertyTagThumbnailImageHeight

Numero di righe in pixel nell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x5021                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagthumbnailbitspersample"></a>PropertyTagThumbnailBitsPerSample

Numero di bit per componente colore nell'immagine di anteprima. Vedere anche [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).



| Informazioni sulle proprietà | Valore |
|-------|-----------------------------------------------------------------|
| Tag   | 0x5022                                                          |
| Tipo  | PropertyTagTypeShort                                            |
| Conteggio | Numero di campioni (componenti) per pixel nell'immagine di anteprima |



 

## <a name="propertytagthumbnailcompression"></a>PropertyTagThumbnailCompression

Schema di compressione usato per i dati dell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5023               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a>PropertyTagThumbnailPhotometricInterp

Come verranno interpretati i dati di Anteprima pixel.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5024               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailimagedescription"></a>PropertyTagThumbnailImageDescription

Stringa di caratteri con terminazione null che specifica il titolo dell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x5025                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagthumbnailequipmake"></a>PropertyTagThumbnailEquipMake

Stringa di caratteri con terminazione null che specifica il produttore delle apparecchiature usate per registrare l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x5026                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagthumbnailequipmodel"></a>PropertyTagThumbnailEquipModel

Stringa di caratteri con terminazione null che specifica il nome del modello o il numero di modello dell'apparecchiatura utilizzata per registrare l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x5027                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagthumbnailstripoffsets"></a>PropertyTagThumbnailStripOffsets

Per ogni striscia nell'immagine di anteprima, l'offset dei byte di tale striscia. Vedere anche [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) e [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x5028                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | Numero di strisce                            |



 

## <a name="propertytagthumbnailorientation"></a>PropertyTagThumbnailOrientation

Orientamento dell'immagine di anteprima in termini di righe e colonne. Vedere anche [PropertyTagOrientation](#propertytagorientation).



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5029               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a>PropertyTagThumbnailSamplesPerPixel

Numero di componenti colore per pixel nell'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x502A               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a>PropertyTagThumbnailRowsPerStrip

Numero di righe per strip nell'immagine di anteprima. Vedere anche [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) e [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x502B                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a>PropertyTagThumbnailStripBytesCount

Per ogni striscia di immagine di anteprima, il numero totale di byte in tale striping.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0x502C                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | Numero di strisce nell'immagine di anteprima     |



 

## <a name="propertytagthumbnailresolutionx"></a>PropertyTagThumbnailResolutionX

Risoluzione delle anteprime nella direzione della larghezza. L'unità di risoluzione viene specificata in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Informazioni sulle proprietà | Valore |
|-----|--------|
| Tag | 0x502D |



 

## <a name="propertytagthumbnailresolutiony"></a>PropertyTagThumbnailResolutionY

Risoluzione dell'anteprima nella direzione dell'altezza. L'unità di risoluzione viene specificata in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Informazioni sulle proprietà | Valore |
|-----|--------|
| Tag | 0x502E |



 

## <a name="propertytagthumbnailplanarconfig"></a>PropertyTagThumbnailPlanarConfig

Indica se i componenti dei pixel nell'immagine di anteprima vengono registrati in formato Chunk o Planar. Vedere anche [PropertyTagPlanarConfig](#propertytagplanarconfig).



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x502F               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailresolutionunit"></a>PropertyTagThumbnailResolutionUnit

Unità di misura per la risoluzione orizzontale e la risoluzione verticale dell'immagine di anteprima. Vedere anche [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5030               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailtransferfunction"></a>PropertyTagThumbnailTransferFunction

Tabelle che specificano le funzioni di trasferimento per l'immagine di anteprima. Vedere anche [PropertyTagTransferFunction](#propertytagtransferfunction).



| Informazioni sulle proprietà | Valore |
|-------|------------------------------------------------------|
| Tag   | 0x5031                                               |
| Tipo  | PropertyTagTypeShort                                 |
| Conteggio | Numero totale di parole a 16 bit necessarie per le tabelle |



 

## <a name="propertytagthumbnailsoftwareused"></a>PropertyTagThumbnailSoftwareUsed

Stringa di caratteri con terminazione null che specifica il nome e la versione del software o del firmware del dispositivo usato per generare l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x5032                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagthumbnaildatetime"></a>PropertyTagThumbnailDateTime

Data e ora di creazione dell'immagine di anteprima. Vedere anche [PropertyTagDateTime](#propertytagdatetime).



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5033               |
| Tipo  | PropertyTagTypeASCII |
| Conteggio | 20                   |



 

## <a name="propertytagthumbnailartist"></a>PropertyTagThumbnailArtist

Stringa di caratteri con terminazione null che specifica il nome della persona che ha creato l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x5034                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagthumbnailwhitepoint"></a>PropertyTagThumbnailWhitePoint

Cromaticità del punto bianco dell'immagine di anteprima. Vedere anche [PropertyTagWhitePoint](#propertytagwhitepoint).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x5035                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 2                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a>PropertyTagThumbnailPrimaryChromaticities

Per ognuno dei tre colori primari nell'immagine di anteprima, la cromaticità di tale colore. Vedere anche [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x5036                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 6                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a>PropertyTagThumbnailYCbCrCoefficients

Coefficienti per la trasformazione da RGB a dati YCbCr per l'immagine di anteprima. Vedere anche [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x5037                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 3                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a>PropertyTagThumbnailYCbCrSubsampling

Rapporto di campionamento dei componenti cromatura in relazione al componente di luminanza per l'immagine di anteprima. Vedere anche [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5038               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 2                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a>PropertyTagThumbnailYCbCrPositioning

Posizione dei componenti cromatura in relazione al componente di luminanza per l'immagine di anteprima. Vedere anche [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5039               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a>PropertyTagThumbnailRefBlackWhite

Valore del punto nero di riferimento e valore del punto bianco di riferimento per l'immagine di anteprima. Vedere anche [PropertyTagREFBlackWhite](#propertytagrefblackwhite).



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x503A                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 6                       |



 

## <a name="propertytagthumbnailcopyright"></a>PropertyTagThumbnailCopyRight

Stringa di caratteri con terminazione null che contiene informazioni sul copyright per l'immagine di anteprima.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x503B                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagluminancetable"></a>PropertyTagLuminanceTable

Tabella luminanza. La tabella luminanza e la tabella cromatura vengono usate per controllare la qualità JPEG. Una tabella luminanza o cromatura valida contiene 64 voci di tipo PropertyTagTypeShort. Se un'immagine include una tabella di luminanza o una tabella cromatura, deve disporre di entrambe le tabelle.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5090               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 64                   |



 

## <a name="propertytagchrominancetable"></a>PropertyTagChrominanceTable

Tabella cromatura. La tabella luminanza e la tabella cromatura vengono usate per controllare la qualità JPEG. Una tabella luminanza o cromatura valida contiene 64 voci di tipo PropertyTagTypeShort. Se un'immagine include una tabella di luminanza o una tabella cromatura, deve disporre di entrambe le tabelle.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5091               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 64                   |



 

## <a name="propertytagframedelay"></a>PropertyTagFrameDelay

Ritardo di tempo, in centesimi di secondo, tra due fotogrammi in un'immagine GIF animata.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------------|
| Tag   | 0x5100                        |
| Tipo  | PropertyTagTypeLong           |
| Conteggio | Numero di frame nell'immagine |



 

## <a name="propertytagloopcount"></a>PropertyTagLoopCount

Per un'immagine GIF animata, il numero di volte in cui visualizzare l'animazione. Il valore 0 indica che l'animazione deve essere visualizzata infinitamente.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x5101               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 1                    |



 

## <a name="propertytagglobalpalette"></a>PropertyTagGlobalPalette

Tavolozza dei colori per una bitmap indicizzata in un'immagine GIF.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------------|
| Tag   | 0x5102                        |
| Tipo  | PropertyTagTypeByte           |
| Conteggio | 3 x numero di voci della tavolozza |



 

## <a name="propertytagindexbackground"></a>PropertyTagIndexBackground

Indice del colore di sfondo nella tavolozza di un'immagine GIF.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5103              |
| Tipo  | PropertyTagTypeByte |
| Conteggio | 1                   |



 

## <a name="propertytagindextransparent"></a>PropertyTagIndexTransparent

Indice del colore trasparente nella tavolozza di un'immagine GIF.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5104              |
| Tipo  | PropertyTagTypeByte |
| Conteggio | 1                   |



 

## <a name="propertytagpixelunit"></a>PropertyTagPixelUnit

Unità per PropertyTagPixelPerUnitX e PropertyTagPixelPerUnitY.



Tag

0x5110

Tipo

PropertyTagTypeByte

Conteggio

1

0-sconosciuto



 

## <a name="propertytagpixelperunitx"></a>PropertyTagPixelPerUnitX

Pixel per unità nella direzione x.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5111              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagpixelperunity"></a>PropertyTagPixelPerUnitY

Pixel per unità nella direzione y.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x5112              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagpalettehistogram"></a>PropertyTagPaletteHistogram

Istogramma tavolozza.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x5113                  |
| Tipo  | PropertyTagTypeByte     |
| Conteggio | Lunghezza dell'istogramma |



 

## <a name="propertytagcopyright"></a>PropertyTagCopyright

Stringa di caratteri con terminazione null che contiene informazioni sul copyright.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x8298                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagexifexposuretime"></a>PropertyTagExifExposureTime

Tempo di esposizione, espresso in secondi.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x829A                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexiffnumber"></a>PropertyTagExifFNumber

Numero F.



| Informazioni sulle proprietà | Valore |
|-------|----------|
| Tag   | 0x829D   |
| Tipo  | RAZIONALE |
| Conteggio | 1        |



 

## <a name="propertytagexififd"></a>PropertyTagExifIFD

Tag privato utilizzato da GDI+. Non per uso pubblico. GDI+ utilizza questo tag per individuare informazioni specifiche di EXIF.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x8769              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagiccprofile"></a>PropertyTagICCProfile

Profilo ICC incorporato nell'immagine.



| Informazioni sulle proprietà | Valore |
|-------|-----------------------|
| Tag   | 0x8773                |
| Tipo  | PropertyTagTypeByte   |
| Conteggio | Lunghezza del profilo |



 

## <a name="propertytagexifexposureprog"></a>PropertyTagExifExposureProg

Classe del programma utilizzata dalla fotocamera per impostare l'esposizione quando viene acquisita l'immagine.



Tag

0x8822

Tipo

SHORT

Conteggio

1

Predefinito

0

0-non definito 1-manuale 2-programma normale 3-priorità di apertura 4-priorità di otturazione 5-programma creativo (distorto verso la profondità del campo) 6-programma di azione (polarizzato verso Fast velocità dell'otturatore) 7-modalità verticale (per le foto di chiusura con lo sfondo non attivo) 8-modalità orizzontale (per le foto paesaggistiche con lo sfondo attivo) da 9 a 255-riservato



 

## <a name="propertytagexifspectralsense"></a>PropertyTagExifSpectralSense

Stringa di caratteri con terminazione null che specifica la sensibilità spettrale di ogni canale della fotocamera usata. La stringa è compatibile con lo standard sviluppato dal comitato tecnico ASTM.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x8824                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytaggpsifd"></a>PropertyTagGpsIFD

Offset a un blocco di elementi di proprietà GPS. Gli elementi di proprietà i cui tag hanno il prefisso PropertyTagGps vengono archiviati nel blocco GPS. Gli elementi delle proprietà GPS sono definiti nella specifica EXIF. GDI+ utilizza questo tag per individuare le informazioni GPS, ma GDI+ non espone questo tag per l'utilizzo pubblico.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0x8825              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagexifisospeed"></a>PropertyTagExifISOSpeed

Velocità ISO e latitudine ISO della fotocamera o del dispositivo di input come specificato in ISO 12232.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x8827               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | Qualsiasi                  |



 

## <a name="propertytagexifoecf"></a>PropertyTagExifOECF

Funzione di conversione optoelettronica (OECF) specificata in ISO 14524. OECF è la relazione tra l'input ottico della fotocamera e i valori di immagine.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x8828                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

## <a name="propertytagexifver"></a>PropertyTagExifVer

Versione dello standard EXIF supportata. La mancata esistenza di questo campo viene utilizzata per indicare la non conformità allo standard. La conformità allo standard è indicata dalla registrazione di 0210 come stringa ASCII a 4 byte. Poiché il tipo è PropertyTagTypeUndefined, non esiste alcun carattere di terminazione NULL.



| Informazioni sulle proprietà | Valore |
|---------|--------------------------|
| Tag     | 0x9000                   |
| Tipo    | PropertyTagTypeUndefined |
| Conteggio   | 4                        |
| Predefinito | 0210                     |



 

## <a name="propertytagexifdtorig"></a>PropertyTagExifDTOrig

Data e ora di generazione dei dati dell'immagine originale. Per un DSC, la data e l'ora in cui è stata acquisita l'immagine. Il formato è aaaa: MM: GG HH: MM: SS con ora indicata nel formato a 24 ore e la data e l'ora separate da un carattere vuoto (0x2000). La lunghezza della stringa di caratteri è 20 byte, incluso il terminatore NULL. Quando il campo è vuoto, viene considerato sconosciuto.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x9003               |
| Tipo  | PropertyTagTypeASCII |
| Conteggio | 20                   |



 

## <a name="propertytagexifdtdigitized"></a>PropertyTagExifDTDigitized

Data e ora in cui l'immagine è stata archiviata come dati digitali. Se, ad esempio, un'immagine è stata acquisita da DSC e nello stesso momento in cui il file è stato registrato, DateTimeOriginal e DateTimeDigitized avranno lo stesso contenuto.

Il formato è aaaa: MM: GG HH: MM: SS con ora indicata nel formato a 24 ore e la data e l'ora separate da un carattere vuoto (0x2000). La lunghezza della stringa di caratteri è 20 byte, incluso il terminatore NULL. Quando il campo è vuoto, viene considerato sconosciuto.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0x9004               |
| Tipo  | PropertyTagTypeASCII |
| Conteggio | 20                   |



 

## <a name="propertytagexifcompconfig"></a>PropertyTagExifCompConfig

Informazioni specifiche per i dati compressi. I canali di ogni componente sono disposti in ordine dal primo componente al quarto. Per i dati non compressi, la disposizione dei dati viene fornita nel tag PropertyTagPhotometricInterp.

Tuttavia, poiché PropertyTagPhotometricInterp è in grado di esprimere solo l'ordine di Y, CB e CR, questo tag viene fornito nei casi in cui i dati compressi utilizzano componenti diversi da Y, CB e CR e per supportare altre sequenze.



Tag

0x9101

Tipo

PropertyTagTypeUndefined

Conteggio

4

Predefinito

4 5 6 0 (se RGB non compresso) 1 2 3 0 (altri casi)

0: non esiste 1-Y 2-CB 3-CR 4-R 5-G 6-B other-reserved



 

## <a name="propertytagexifcompbpp"></a>PropertyTagExifCompBPP

Informazioni specifiche per i dati compressi. La modalità di compressione utilizzata per un'immagine compressa è indicata in unità BPP.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x9102                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifshutterspeed"></a>PropertyTagExifShutterSpeed

Velocità dell'otturatore. L'unità è il valore di sistema additivo per l'esposizione fotografica (apice).



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x9201                   |
| Tipo  | PropertyTagTypeSRational |
| Conteggio | 1                        |



 

## <a name="propertytagexifaperture"></a>PropertyTagExifAperture

Apertura dell'obiettivo. L'unità è il valore apice.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x9202                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifbrightness"></a>PropertyTagExifBrightness

Valore di luminosità. L'unità è il valore apice. Normalmente viene specificato nell'intervallo compreso tra-99,99 e 99,99.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x9203                   |
| Tipo  | PropertyTagTypeSRational |
| Conteggio | 1                        |



 

## <a name="propertytagexifexposurebias"></a>PropertyTagExifExposureBias

Distorsione dell'esposizione. L'unità è il valore apice. Normalmente viene specificato nell'intervallo compreso tra-99,99 e 99,99.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x9204                   |
| Tipo  | PropertyTagTypeSRational |
| Conteggio | 1                        |



 

## <a name="propertytagexifmaxaperture"></a>PropertyTagExifMaxAperture

Numero F più piccolo dell'obiettivo. L'unità è il valore apice. Normalmente viene specificato nell'intervallo compreso tra 00,00 e 99,99, ma non è limitato a questo intervallo.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x9205                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifsubjectdist"></a>PropertyTagExifSubjectDist

Distanza al soggetto, misurata in metri.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x9206                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifmeteringmode"></a>PropertyTagExifMeteringMode

Modalità di misurazione.



Tag

0x9207

Tipo

PropertyTagTypeShort

Conteggio

1

Predefinito

0

0: Unknown 1-Average 2-CenterWeightedAverage 3-spot 4-multispot 5-pattern 6-partial 7 to 254-reserved 255-other



 

## <a name="propertytagexiflightsource"></a>PropertyTagExifLightSource

Tipo di origine di luce.



Tag

0x9208

Tipo

PropertyTagTypeShort

Conteggio

1

Predefinito

0

0-Unknown 1-Daylight 2-fluorescente 3-Tungsten 17-standard Light A 18-standard Light B 19-standard Light C 20-D55 21-D65 22-D75 23 to 254-reserved 255-other



 

## <a name="propertytagexifflash"></a>PropertyTagExifFlash

Stato del flash. Questo tag viene registrato quando un'immagine viene eseguita utilizzando una luce stroboscopica (Flash). Il bit 0 indica lo stato di attivazione del flash e i bit 1 e 2 indicano lo stato di restituzione del flash.



Tag

0x9209

Tipo

PropertyTagTypeShort

Conteggio

1

Valori per bit 0 che indicano se il flash generato: 0B-Flash non ha attivato 1B-Flash attivato

Valori per BITS 1 e 2 che indicano lo stato della luce restituita: 00B-nessuna funzione di rilevamento del ritorno stroboscopio 01B-riservato 10B-Strobe return Light non rilevato 11b-Strobe return light rilevato

Valori dei tag flash derivati: 0x0000-Flash non ha attivato 0x0001-Flash fired 0x0005-Strobe return Light non rilevato



 

## <a name="propertytagexiffocallength"></a>PropertyTagExifFocalLength

Lunghezza focale effettiva, in millimetri, della lente. La conversione non viene eseguita alla lunghezza focale di una fotocamera a pellicola 35 millimetri.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0x920A                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifmakernote"></a>PropertyTagExifMakerNote

Tag di nota. Tag utilizzato dai produttori dei writer EXIF per registrare le informazioni. Il contenuto spetta al produttore.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x927C                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

## <a name="propertytagexifusercomment"></a>PropertyTagExifUserComment

Tag di commento. Tag utilizzato dagli utenti EXIF per scrivere parole chiave o commenti sull'immagine oltre a quelli presenti in PropertyTagImageDescription e senza le limitazioni del codice carattere del tag PropertyTagImageDescription.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0x9286                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

Il codice carattere usato nel tag PropertyTagExifUserComment viene identificato in base a un codice ID in un'area fissa a 8 byte all'inizio dell'area dati del tag. La parte inutilizzata dell'area viene riempita con caratteri null (0). I codici ID vengono assegnati per mezzo della registrazione. Poiché il tipo non è ASCII, non è necessario usare un carattere di terminazione NULL.

## <a name="propertytagexifdtsubsec"></a>PropertyTagExifDTSubsec

Stringa di caratteri con terminazione null che specifica una frazione di secondo per il tag PropertyTagDateTime.



| Informazioni sulle proprietà | Valore |
|-------|----------------------------------------------------|
| Tag   | 0x9290                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Conteggio | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagexifdtorigss"></a>PropertyTagExifDTOrigSS

Stringa di caratteri con terminazione null che specifica una frazione di secondo per il tag PropertyTagExifDTOrig.



| Informazioni sulle proprietà | Valore |
|------|----------------------------------------------------|
| Tag  | 0x9291                                             |
| Tipo | PropertyTagTypeASCII                               |
| N    | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagexifdtdigss"></a>PropertyTagExifDTDigSS

Stringa di caratteri con terminazione null che specifica una frazione di secondo per il tag PropertyTagExifDTDigitized.



| Informazioni sulle proprietà | Valore |
|------|----------------------------------------------------|
| Tag  | 0x9292                                             |
| Tipo | ASCII                                              |
| N    | Lunghezza della stringa che include il carattere di terminazione NULL |



 

## <a name="propertytagexiffpxver"></a>PropertyTagExifFPXVer

Versione del formato FlashPix supportata da un file FPXR. Se la funzione FPXR supporta la versione 1,0 del formato FlashPix, questo è indicato in modo analogo a PropertyTagExifVer registrando 0100 come stringa ASCII a 4 byte. Poiché il tipo è PropertyTagTypeUndefined, non esiste alcun carattere di terminazione NULL.



Tag

0xA000

Tipo

PropertyTagTypeUndefined

Conteggio

4

Predefinito

0100

0100-FlashPix formato versione 1,0 altro-riservato



 

## <a name="propertytagexifcolorspace"></a>PropertyTagExifColorSpace

Identificatore dello spazio colori. Normalmente sRGB (= 1) viene utilizzato per definire lo spazio dei colori in base alle condizioni di monitoraggio del PC e all'ambiente. Se viene utilizzato uno spazio dei colori diverso da sRGB, viene impostato uncalibrato (= 0xFFFF). I dati dell'immagine registrati come non calibrati possono essere considerati come sRGB quando vengono convertiti in FlashPix.



Tag

0xA001

Tipo

PropertyTagTypeShort

Conteggio

1

0x1-sRGB 0xFFFF-uncalibred other-reserved



 

## <a name="propertytagexifpixxdim"></a>PropertyTagExifPixXDim

Informazioni specifiche per i dati compressi. Quando viene registrato un file compresso, la larghezza valida dell'immagine significativa deve essere registrata in questo tag, indipendentemente dal fatto che siano presenti dati di riempimento o un marcatore di riavvio. Questo tag non deve esistere in un file non compresso.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0xA002                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagexifpixydim"></a>PropertyTagExifPixYDim

Informazioni specifiche per i dati compressi. Quando viene registrato un file compresso, l'altezza valida dell'immagine significativa deve essere registrata in questo tag se sono presenti o meno dati di riempimento o un marcatore di riavvio. Questo tag non deve esistere in un file non compresso. Poiché la spaziatura interna dei dati non è necessaria nella direzione verticale, il numero di righe registrate in questo tag di altezza dell'immagine valido sarà identico a quello registrato in SOF.



| Informazioni sulle proprietà | Valore |
|-------|---------------------------------------------|
| Tag   | 0xA003                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Conteggio | 1                                           |



 

## <a name="propertytagexifrelatedwav"></a>PropertyTagExifRelatedWav

Nome di un file audio correlato ai dati dell'immagine. Le uniche informazioni relazionali registrate sono il nome e l'estensione del file audio EXIF, ovvero una stringa ASCII costituita da 8 caratteri e un punto (.), più 3 caratteri. Il percorso non viene registrato. Quando si usa questo tag, i file audio devono essere registrati in conformità con il formato audio EXIF. I writer possono inoltre archiviare dati audio all'interno di APP2 come dati del flusso di estensione FlashPix.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0xA004               |
| Tipo  | PropertyTagTypeASCII |
| Conteggio | 13                   |



 

## <a name="propertytagexifinterop"></a>PropertyTagExifInterop

Offset a un blocco di elementi di proprietà che contengono informazioni di interoperabilità.



| Informazioni sulle proprietà | Valore |
|-------|---------------------|
| Tag   | 0xA005              |
| Tipo  | PropertyTagTypeLong |
| Conteggio | 1                   |



 

## <a name="propertytagexifflashenergy"></a>PropertyTagExifFlashEnergy

Energia stroboscopica, in secondi di potenza candela (BCPS), nel momento in cui l'immagine è stata acquisita.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0xA20B                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifspatialfr"></a>PropertyTagExifSpatialFR

La tabella o la frequenza spaziale del dispositivo di input e i valori SFR nella larghezza dell'immagine, nell'altezza dell'immagine e nella direzione diagonale, come specificato in ISO 12233.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0xA20C                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

## <a name="propertytagexiffocalxres"></a>PropertyTagExifFocalXRes

Numero di pixel nella direzione della larghezza dell'immagine (x) per unità sul piano focale della fotocamera. L'unità viene specificata in PropertyTagExifFocalResUnit.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0xA20E                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexiffocalyres"></a>PropertyTagExifFocalYRes

Numero di pixel nella direzione altezza (y) immagine per unità sul piano focale della fotocamera. L'unità viene specificata in PropertyTagExifFocalResUnit.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0xA20F                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexiffocalresunit"></a>PropertyTagExifFocalResUnit

Unità di misura per PropertyTagExifFocalXRes e PropertyTagExifFocalYRes.



Tag

0xA210

Tipo

PropertyTagTypeShort

Conteggio

1

2-pollice 3 centimetri



 

## <a name="propertytagexifsubjectloc"></a>PropertyTagExifSubjectLoc

Posizione dell'oggetto principale nella scena. Il valore di questo tag rappresenta il pixel al centro dell'oggetto principale relativo al bordo sinistro. Il primo valore indica il numero di colonna e il secondo valore indica il numero di riga.



| Informazioni sulle proprietà | Valore |
|-------|----------------------|
| Tag   | 0xA214               |
| Tipo  | PropertyTagTypeShort |
| Conteggio | 2                    |



 

## <a name="propertytagexifexposureindex"></a>PropertyTagExifExposureIndex

Indice di esposizione selezionato nella fotocamera o nel dispositivo di input nel momento in cui l'immagine è stata acquisita.



| Informazioni sulle proprietà | Valore |
|-------|-------------------------|
| Tag   | 0xA215                  |
| Tipo  | PropertyTagTypeRational |
| Conteggio | 1                       |



 

## <a name="propertytagexifsensingmethod"></a>PropertyTagExifSensingMethod

Tipo di sensore immagine nella fotocamera o nel dispositivo di input.



Tag

0xA217

Tipo

PropertyTagTypeShort

Conteggio

1

1-non definito 2-un sensore area colori a un chip 3-sensore area colore a due chip 4-sensore area colori a tre chip 5-colore sensore area di colore 7-sensore trilineario 8-sensore lineare sequenziale altro-riservato



 

## <a name="propertytagexiffilesource"></a>PropertyTagExifFileSource

Origine dell'immagine. Se un DSC ha registrato l'immagine, il valore di questo tag è 3.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0xA300                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | 1                        |



 

## <a name="propertytagexifscenetype"></a>PropertyTagExifSceneType

Tipo di scena. Se un DSC ha registrato l'immagine, il valore del tag deve essere impostato su 1, a indicare che l'immagine è stata fotografata direttamente.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0xA301                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | 1                        |



 

## <a name="propertytagexifcfapattern"></a>PropertyTagExifCfaPattern

Modello geometrico della matrice di filtri colori (CFA) del sensore di immagine quando viene usato un sensore di area colore a un chip. Non si applica a tutti i metodi di rilevamento.



| Informazioni sulle proprietà | Valore |
|-------|--------------------------|
| Tag   | 0xA302                   |
| Tipo  | PropertyTagTypeUndefined |
| Conteggio | Qualsiasi                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifiche di formato dei file di immagine](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Costanti Tag proprietà immagine](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[**Costanti del tipo di tag della proprietà Image**](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[Tag di proprietà in ordine alfabetico](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[Tag di proprietà in ordine numerico](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[Lettura e scrittura di metadati](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



