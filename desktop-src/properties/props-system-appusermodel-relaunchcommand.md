---
description: Specifica un comando che può essere eseguito tramite ShellExecute per avviare un'applicazione quando viene aggiunta alla barra delle applicazioni o quando viene avviata una nuova istanza dell'applicazione tramite il Jump List dell'applicazione.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System.AppUserModel.RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2ce3783aa9ab3d76124b8d62f9d9d9ad2e1f5d4b92622716df111456dbabd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554521"
---
# <a name="systemappusermodelrelaunchcommand"></a>System.AppUserModel.RelaunchCommand

Specifica un comando che può essere eseguito tramite [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare un'applicazione quando viene aggiunta alla barra delle applicazioni o quando viene avviata una nuova istanza dell'applicazione tramite il Jump List dell'applicazione.

Negli esempi vengono illustrati gli aspetti seguenti:


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Questa proprietà viene usata solo se una finestra ha un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se la finestra non ha un AppUserModelID esplicito, questa proprietà viene ignorata e la finestra viene raggruppata e aggiunta come se fosse parte del processo proprietario. Per altre informazioni sull'applicazione di AppUserModelIDs espliciti e sul relativo effetto sull'aggiunta alla barra delle applicazioni, vedere ID modello utente applicazione [(AppUserModelIDs).](../shell/appids.md)

Questa proprietà deve essere utilizzata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite.

> [!Note]  
> [System.AppUserModel.RelaunchCommand]() e [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) devono sempre essere impostati insieme. Se una di queste proprietà non è impostata, non viene usata nessuna delle due proprietà.

 

Questa proprietà, insieme a [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) e [System.AppUserModel.RelaunchIconResource,](./props-system-appusermodel-relaunchiconresource.md) può essere usata per definire visivamente una finestra come applicazione per l'utente. Ciò è utile per gli scenari di applicazioni host, in cui una singola istanza host esegue più applicazioni figlio. Ad esempio, una macchina virtuale che ospita diverse applicazioni virtualizzate potrebbe richiedere che tali applicazioni virtualizzate vengano visualizzate come singole applicazioni per l'utente. La macchina virtuale può etichettare ogni finestra con un AppUserModelID esplicito e le proprietà di riavvio appropriate per renderle visualizzate come applicazioni. L'utente può quindi bloccarli sulla barra delle applicazioni e "riavviare" l'istanza bloccata.

> [!Note]  
> Questa proprietà viene ignorata [se System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) è impostato. In questo modo un'applicazione può controllare il raggruppamento delle finestre assegnando loro appUserModelID espliciti, impedendo però che tali finestre vengano bloccate.

 

Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System.AppUserModel.RelaunchCommand]() di tale finestra.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
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

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
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

 

 
