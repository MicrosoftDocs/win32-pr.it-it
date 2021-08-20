---
description: ID modello utente applicazione esplicito (AppUserModelID) usato per associare processi, file e finestre a una particolare applicazione.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd60b64598a620221ec2b610b10cbc05002f38aaf633e51e788b24797620cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033739"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

ID modello utente applicazione esplicito (AppUserModelID) usato per associare processi, file e finestre a una particolare applicazione. In alcuni casi, è sufficiente fare affidamento sull'AppUserModelID interno assegnato a un processo dal sistema. Tuttavia, un'applicazione proprietaria di più processi o un'applicazione in esecuzione in un processo host potrebbe dover identificarsi in modo esplicito tramite questa proprietà in modo che possa raggruppare le finestre altrimenti diverse sotto un singolo pulsante della barra delle applicazioni e controllare il contenuto del Jump List dell'applicazione.

Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System.AppUserModel.ID]() di tale finestra.

Per altre informazioni, vedere [ID modello utente applicazione (AppUserModelIDs).](../shell/appids.md)

Quando la proprietà [System.AppUserModel.ID]() è impostata, alla barra delle applicazioni viene notificato di aggiornare le informazioni sulla finestra o sul collegamento in base all'AppUserModelID.

Altre proprietà di finestra e collegamento possono essere usate insieme a un AppUserModelID esplicito per controllare ulteriormente il raggruppamento e l'aggiunta associati a una finestra, il nome visualizzato e l'icona usati nella barra delle applicazioni e il comando per avviare un'applicazione aggiunta alla barra delle applicazioni o una nuova istanza dell'applicazione tramite il Jump List dell'applicazione. Queste proprietà devono essere impostate prima di impostare [System.AppUserModel.ID]() proprietà . Per altre informazioni, vedere i seguenti argomenti:

-   [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md)
-   [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelID)](../shell/appids.md)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[proprietàDescrizione](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
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

[Enum](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
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

 

 
