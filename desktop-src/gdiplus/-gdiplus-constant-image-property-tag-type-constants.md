---
description: È possibile archiviare e recuperare i metadati dell'immagine con l'aiuto di un oggetto PropertyItem. Il membro dati type di un oggetto PropertyItem specifica il tipo di dati dei valori archiviati nel membro dati value dello stesso oggetto PropertyItem.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Costanti del tipo di tag di proprietà Image (Gdiplusimaging.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb565972b2dc8b8962e367c7d2f3c09b4f857382156538a83f7d6ee338c66ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977601"
---
# <a name="image-property-tag-type-constants"></a>Costanti del tipo di tag di proprietà Image

È possibile archiviare e recuperare i metadati dell'immagine con l'aiuto di un [**oggetto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) Il **membro** dati type di **un oggetto PropertyItem** specifica il tipo di dati dei valori archiviati nel membro dati value dello stesso oggetto **PropertyItem.**

Le costanti seguenti, definite in Gdiplusimaging.h, possono  essere assegnate al membro dati di tipo di un [**oggetto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)



| Costante                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Specifica che il formato è di 4 bit per pixel indicizzati.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**PropertyTagTypeASCII**</dt> </dl>                 | Specifica che il membro **dati value** è una stringa ASCII con terminazione Null. Se si  imposta il membro dati di tipo di un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) su PropertyTagTypeASCII, è necessario impostare il membro dati **length** sulla lunghezza della stringa, incluso il carattere di terminazione NULL. Ad esempio, la stringa `HELLO` avrebbe una lunghezza pari a 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**PropertyTagTypeByte**</dt> </dl>                     | Specifica che il membro **dati value** è una matrice di byte.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**PropertyTagTypeLong**</dt> </dl>                     | Specifica che il membro **dati value** è una matrice di interi senza segno long (32 bit).<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**PropertyTagTypeRational**</dt> </dl>     | Specifica che il membro **dati value** è una matrice di coppie di interi lunghi senza segno. Ogni coppia rappresenta una frazione; il primo intero è il numeratore e il secondo è il denominatore.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**PropertyTagTypeShort**</dt> </dl>                 | Specifica che il membro **dati value** è una matrice di interi unsigned short (a 16 bit).<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | Specifica che il membro **dati value** è una matrice di interi con segno long (32 bit).<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | Specifica che il membro **dati value** è una matrice di coppie di interi lunghi con segno. Ogni coppia rappresenta una frazione; il primo intero è il numeratore e il secondo è il denominatore.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**PropertyTagTypeUndefined**</dt> </dl> | Specifica che il membro **dati value** è una matrice di byte che può contenere valori di qualsiasi tipo di dati. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Gdiplusimaging.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dei tag delle proprietà Image](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Specifiche di formato dei file di immagine](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Lettura e scrittura di metadati](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
