---
description: Data di acquisizione del file o del supporto.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System.DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a78ae9ccfe938551ab6c4a265972e48c3aad1c1791f02cfa933c583c6d4b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599181"
---
# <a name="systemdateacquired"></a>System.DateAcquired

Data di acquisizione del file o del supporto. Questa proprietà è correlata a un determinato utente o gruppo di utenti. Ad esempio, questi dati vengono usati come asse di ordinamento principale per la cartella virtuale **New Musica**, che consente agli utenti di esplorare le aggiunte più recenti alla raccolta.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

[DateAcquired]() viene archiviato come valore nel flusso principale del file, ma potrebbe non essere sempre presente. In questi casi, la data di acquisizione può essere approssimata in base ad altre date note per il contenuto. Il gestore dei metadati deve usare un set di regole per determinare la data da restituire. L'esempio seguente illustra questa operazione per i file musicali.

-   Per la musica acquistata, è consigliabile usare l'ora di creazione del file se non è presente alcuna data acquisita. Tuttavia, il provider di download deve impostare la [proprietà DateAcquired]() nel file.
-   Per i file musicali che l'utente o il gruppo ha "derubato" (copiando musica o video da un CD o DVD a un disco rigido), la data di acquisizione deve essere la data in cui è stata eseguita l'azione. Ad esempio, [l'attributo WM/EncodingTime.](../wmp/wm-encodingtime-attribute.md)
-   Per la musica copiata da un'altra posizione, l'ora di creazione del file deve essere usata come data di acquisizione.

Esempi di [System.DateAcquired]() sono la data e l'ora in cui le immagini vengono acquisite da una fotocamera o quando la musica viene acquistata online. Non è uguale a [System.DateImported](./props-system-dateimported.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[Datetimeformat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
