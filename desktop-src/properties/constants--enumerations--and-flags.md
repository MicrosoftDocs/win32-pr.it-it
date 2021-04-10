---
description: In questa sezione vengono descritte le costanti, le enumerazioni e i flag del sistema di proprietà di Windows.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Costanti, enumerazioni e flag (sistema di proprietà di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8681c773181b69b24b1fe2d01d380d730c33e220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231762"
---
# <a name="constants-enumerations-and-flags"></a>Costanti, enumerazioni e flag

In questa sezione vengono descritte le costanti, le enumerazioni e i flag del sistema di proprietà di Windows.



| Argomento                                                                              | Contenuto                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indica i flag che modificano l'oggetto archivio delle proprietà recuperato da metodi che creano un archivio delle proprietà, ad esempio [**IShellItem2:: GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) o [**IPropertyStoreFactory:: GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Fornisce flag di stato dell'operazione.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**\_flag PKA**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Descrive il comportamento della matrice delle modifiche della proprietà.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_tipo di aggregazione PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Viene descritto come visualizzare i valori delle proprietà quando sono selezionati più elementi. Per una particolare proprietà, il \_ tipo di aggregazione PROPDESC \_ descrive come la proprietà deve essere visualizzata quando vengono selezionati più elementi con un valore per la proprietà, ad esempio se i valori devono essere sommati o calcolati in media, oppure solo visualizzati con la stringa "più valori" predefinita.<br/> |
| [**tipo di PROPDESC \_ COLUMNINDEX \_**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indica se una proprietà può essere indicizzata o meno.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**\_tipo di condizione PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Descrive il tipo di condizione da utilizzare quando si visualizza la proprietà nell'interfaccia utente del generatore di query in Windows Vista, ma non in Windows 7 e versioni successive.<br/>                                                                                                                                                                                                                                      |
| [**\_ENUMFILTER PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Descrive l'elenco filtrato di descrizioni di proprietà restituite.<br/>                                                                                                                                                                                                                                                                                                          |
| [**\_flag di formato PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Utilizzato dalle funzioni di supporto della descrizione della proprietà, ad esempio [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay), per indicare il formato di una stringa di proprietà.<br/>                                                                                                                                                                                                                         |
| [**\_tipo di RELATIVEDESCRIPTION PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Descrive il tipo di descrizione relativo per una descrizione di proprietà, come determinato dall'attributo *relativeDescriptionType* dell'elemento [displayInfo](./propdesc-schema-displayinfo.md) .<br/>                                                                                                                                                                                   |
| [**\_flag SEARCHINFO \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Determina se e come una proprietà viene indicizzata da ricerca di Windows.<br/>                                                                                                                                                                                                                                                                                                             |
| [**\_flag di tipo PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Descrive gli attributi dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md) nel file con estensione propdesc della proprietà.<br/>                                                                                                                                                                                                                                                                |
| [**\_flag di visualizzazione PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Questi flag descrivono le proprietà nelle stringhe dell'elenco di descrizioni della proprietà.<br/>                                                                                                                                                                                                                                                                                                           |
| [**\_flag PROPERTYUI**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Specifica le funzionalità della proprietà.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**\_unità di confronto PROPVAR \_**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Questi flag sono associati a determinati confronti di strutture [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .<br/>                                                                                                                                                                                                                                                                               |
| [**\_stato PSC**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Specifica lo stato di una proprietà. Sono impostate manualmente dal codice che ospita la cache dell'archivio delle proprietà in memoria.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà Windows](props.md)
</dt> <dt>

[Schema Descrizione proprietà](property-description-schema.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> <dt>

[Interfacce](interfaces.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> <dt>

[Strutture](structures.md)
</dt> </dl>

 

 
