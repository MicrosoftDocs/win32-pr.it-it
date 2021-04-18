---
description: In questa sezione vengono descritte le interfacce del sistema di proprietà di Windows.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfacce (sistema di proprietà di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5003458683fb9b2443df0301676b601901817d54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312559"
---
# <a name="interfaces-windows-property-system"></a>Interfacce (sistema di proprietà di Windows)

In questa sezione vengono descritte le interfacce del sistema di proprietà di Windows.



| Argomento                                                                                        | Contenuto                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Espone un metodo che incapsula una modifica a una singola proprietà.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Espone metodi per diverse operazioni di modifica che possono essere passate a [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation).                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Espone metodi che enumerano e recuperano i dettagli della descrizione delle singole proprietà.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Espone metodi che enumerano e recuperano i dettagli della descrizione delle singole proprietà.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Espone i metodi per ottenere le proprietà delle colonne "Ordina per" per un elemento. Questa interfaccia viene utilizzata dagli oggetti dell'interfaccia utente che desiderano recuperare le colonne di ordinamento primarie o secondarie per una determinata proprietà.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Espone metodi che estraggono informazioni da una raccolta di descrizioni di proprietà presentate come elenco.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Fornisce un metodo che Retrives un'interfaccia [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Espone le informazioni correlate alla ricerca per una proprietà. Le informazioni fornite da questa interfaccia provengono dallo schema [PropertyDescription](./propdesc-schema-propertydescription.md) , elemento [searchInfo](./propdesc-schema-searchinfo.md) per una determinata proprietà. Queste informazioni vengono utilizzate dall'indicizzatore di ricerca di Windows. Per la maggior parte delle applicazioni di chiamata non è necessario chiamare questa interfaccia. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Espone i metodi che estraggono i dati dalle informazioni di enumerazione. [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) consente di accedere agli elementi [enum](./propdesc-schema-enum.md) e [enumRange](./propdesc-schema-enumrange.md) nello [schema proprietà](./propdesc-schema-entry.md) in modo programmatico in fase di esecuzione.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Espone i metodi che estraggono i dati dalle informazioni di enumerazione. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) estende [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Espone metodi che enumerano i valori possibili per una proprietà.                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Espone metodi per l'enumerazione, il recupero e l'impostazione dei valori delle proprietà.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Espone metodi che consentono a un gestore di gestire vari stati per ogni proprietà.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Espone un metodo che determina se una proprietà può essere modificata dall'utente nell'interfaccia utente.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Espone i metodi per ottenere un oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Espone metodi che ottengono descrizioni di proprietà, registrano e annullano la registrazione di schemi di proprietà, enumerano le descrizioni delle proprietà e formattano i valori delle proprietà in modo che sia rigoroso dal tipo.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Gli sviluppatori devono invece usare [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà Windows](props.md)
</dt> <dt>

[Schema Descrizione proprietà](property-description-schema.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> <dt>

[Strutture](structures.md)
</dt> <dt>

[Costanti, enumerazioni e flag](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
