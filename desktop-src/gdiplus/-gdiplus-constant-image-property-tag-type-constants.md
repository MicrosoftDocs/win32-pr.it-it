---
description: È possibile archiviare e recuperare i metadati delle immagini con l'ausilio di un oggetto PropertyItem. Il membro dati del tipo di un oggetto PropertyItem specifica il tipo di dati dei valori archiviati nel membro dati del valore dello stesso oggetto PropertyItem.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Costanti del tipo di tag della proprietà Image (Gdiplusimaging. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1870ad117d8c6f84af9e48f88e94f812c59467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996481"
---
# <a name="image-property-tag-type-constants"></a>Costanti del tipo di tag della proprietà Image

È possibile archiviare e recuperare i metadati delle immagini con l'ausilio di un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) . Il membro dati del **tipo** di un oggetto **PropertyItem** specifica il tipo di dati dei valori archiviati nel membro dati del valore dello stesso oggetto **PropertyItem** .

Le costanti seguenti, definite in Gdiplusimaging. h, possono essere assegnate al membro dati del **tipo** di un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .



| Costante                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Specifica che il formato è di 4 bit per pixel indicizzati.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**PropertyTagTypeASCII**</dt> </dl>                 | Specifica che il membro dati del **valore** è una stringa ASCII con terminazione null. Se si imposta il membro dati del **tipo** di un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) su PropertyTagTypeASCII, è necessario impostare il membro dati **length** sulla lunghezza della stringa, incluso il carattere di terminazione null. Ad esempio, la stringa `HELLO` avrà una lunghezza pari a 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**PropertyTagTypeByte**</dt> </dl>                     | Specifica che il membro dati del **valore** è una matrice di byte.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**PropertyTagTypeLong**</dt> </dl>                     | Specifica che il membro dati del **valore** è una matrice di interi senza segno (a 32 bit).<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**PropertyTagTypeRational**</dt> </dl>     | Specifica che il membro dati del **valore** è una matrice di coppie di interi senza segno. Ogni coppia rappresenta una frazione; il primo numero intero è il numeratore e il secondo Integer è il denominatore.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**PropertyTagTypeShort**</dt> </dl>                 | Specifica che il membro dati del **valore** è una matrice di interi senza segno (a 16 bit).<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | Specifica che il membro dati del **valore** è una matrice di interi con segno lungo (32 bit).<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | Specifica che il membro dati del **valore** è una matrice di coppie di integer long con segno. Ogni coppia rappresenta una frazione; il primo numero intero è il numeratore e il secondo Integer è il denominatore.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**PropertyTagTypeUndefined**</dt> </dl> | Specifica che il membro dati del **valore** è una matrice di byte che può conservare i valori di qualsiasi tipo di dati. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Gdiplusimaging. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Tag proprietà immagine](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Specifiche di formato dei file di immagine](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Lettura e scrittura di metadati](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
