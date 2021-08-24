---
description: In questa sezione vengono descritte le Windows, le enumerazioni e i flag del sistema di proprietà.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Costanti, enumerazioni e flag (Windows proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e39d357ae741ae49c4fa98c886e8c08b3594a2ea3a7e4e045def96abe8c2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718210"
---
# <a name="constants-enumerations-and-flags"></a>Costanti, enumerazioni e flag

In questa sezione vengono descritte le Windows, le enumerazioni e i flag del sistema di proprietà.



| Argomento                                                                              | Contenuto                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indica flag che modificano l'oggetto archivio proprietà recuperato dai metodi che creano un archivio proprietà, ad esempio [**IShellItem2::GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) o [**IPropertyStoreFactory::GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Fornisce i flag di stato dell'operazione.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**FLAG \_ PKA**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Descrive il comportamento della matrice di modifiche delle proprietà.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**TIPO DI AGGREGAZIONE \_ \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Descrive come vengono visualizzati i valori delle proprietà quando vengono selezionati più elementi. Per una particolare proprietà, PROPDESC AGGREGATION TYPE descrive come visualizzare la proprietà quando vengono selezionati più elementi con un valore per la proprietà, ad esempio se i valori devono essere sommati o mediati o semplicemente visualizzati con la stringa \_ \_ predefinita "Più valori".<br/> |
| [**TIPO PROPDESC \_ \_ COLUMNINDEX**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indica se una proprietà può essere indicizzata o meno.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**TIPO DI CONDIZIONE \_ \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Descrive il tipo di condizione da usare quando si visualizza la proprietà nell'interfaccia utente del generatore di query in Windows Vista, ma non in Windows 7 e versioni successive.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Descrive l'elenco filtrato delle descrizioni delle proprietà restituite.<br/>                                                                                                                                                                                                                                                                                                          |
| [**FLAG DI FORMATO PROPDESC \_ \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Usato dalle funzioni helper di descrizione della proprietà, ad [**esempio PSFormatForDisplay,**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)per indicare il formato di una stringa di proprietà.<br/>                                                                                                                                                                                                                         |
| [**TIPO PROPDESC \_ RELATIVEDESCRIPTION \_**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Descrive il tipo di descrizione relativa per una descrizione della proprietà, come determinato *dall'attributo relativeDescriptionType* dell'elemento [displayInfo.](./propdesc-schema-displayinfo.md)<br/>                                                                                                                                                                                   |
| [**FLAG PROPDESC \_ SEARCHINFO \_**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Determina se e come una proprietà viene indicizzata da Windows ricerca.<br/>                                                                                                                                                                                                                                                                                                             |
| [**FLAG DI TIPO PROPDESC \_ \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Descrive gli attributi [dell'elemento typeInfo](./propdesc-schema-typeinfo.md) nel file propdesc della proprietà.<br/>                                                                                                                                                                                                                                                                |
| [**FLAG DI VISUALIZZAZIONE PROPDESC \_ \_**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Questi flag descrivono le proprietà nelle stringhe dell'elenco di descrizione delle proprietà.<br/>                                                                                                                                                                                                                                                                                                           |
| [**FLAG \_ PROPERTYUI**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Specifica le funzionalità delle proprietà.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**PROPVAR \_ COMPARE \_ UNIT**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Questi flag sono associati a determinati confronti di strutture [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)<br/>                                                                                                                                                                                                                                                                               |
| [**STATO \_ PSC**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Specifica lo stato di una proprietà. Vengono impostate manualmente dal codice che ospita la cache dell'archivio delle proprietà in memoria.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà Windows](props.md)
</dt> <dt>

[Schema di descrizione della proprietà](property-description-schema.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> <dt>

[Interfacce](interfaces.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> <dt>

[Strutture](structures.md)
</dt> </dl>

 

 
