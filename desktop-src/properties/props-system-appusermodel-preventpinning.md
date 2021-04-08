---
description: Disabilita la possibilità di aggiungere un collegamento o una finestra alla barra delle applicazioni o al menu Start. Questa proprietà rende anche l'elemento non idoneo per l'inclusione nell'elenco dei menu Start (MFU) usato più di frequente.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882209"
---
# <a name="systemappusermodelpreventpinning"></a>System. AppUserModel. PreventPinning

Disabilita la possibilità di aggiungere un collegamento o una finestra alla barra delle applicazioni o al menu **Start** . Questa proprietà rende anche l'elemento non idoneo per l'inclusione nell'elenco dei menu **Start** (MFU) usato più di frequente.

Questa proprietà deve essere impostata su una finestra prima della [proprietà \_ \_ ID AppUserModel pkey](./props-system-appusermodel-id.md) . Una volta \_ impostata la proprietà pkey AppUserModel \_ ID, le modifiche apportate a [pkey \_ AppUserModel \_ PreventPinning]() vengono ignorate.

Per ulteriori informazioni sugli ID del modello utente dell'applicazione (AppUserModelIDs) e altri metodi di esclusione di un elemento da aggiungere alla barra delle applicazioni e dall'inclusione MFU, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md).

Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System. AppUserModel. PreventPinning]() di tale finestra.

Se si imposta questa proprietà, le proprietà seguenti verranno ignorate:

-   [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[enum](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
