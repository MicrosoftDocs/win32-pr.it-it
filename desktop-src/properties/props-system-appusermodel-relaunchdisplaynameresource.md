---
description: Specifica il nome visualizzato utilizzato per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o di avviare una nuova istanza tramite la Jump List del relativo pulsante.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231602"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System. AppUserModel. RelaunchDisplayNameResource

Specifica il nome visualizzato utilizzato per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o di avviare una nuova istanza tramite la Jump List del relativo pulsante. Il valore di questa proprietà deve essere uno dei seguenti:

-   Stringa di risorsa indiretta, ad esempio "@% systemdir% \\ system32 \\shell32.dll,-19263". Si noti che il carattere ' @' è necessario per distinguere una stringa indiretta da una stringa di testo normale, descritta nel paragrafo successivo. Questa stringa indiretta è costituita da un file binario e da un ID di risorsa della stringa contenuta nel file binario. Si consiglia vivamente di utilizzare questo formato stringa indiretto, che garantisce che il nome visualizzato venga modificato in modo appropriato quando la lingua di sistema viene modificata tramite l'interfaccia utente multilingue (MUI). Il carattere '-' prima dell'ID risorsa è obbligatorio.
-   Una stringa di testo normale che non punta a una risorsa. Questa operazione deve essere usata solo quando il nome visualizzato viene calcolato in modo dinamico o ottenuto da un'origine dati che non supporta MUI. Ad esempio, la stringa può essere il nome di un dispositivo, ad esempio "Microsoft Zune", nei casi in cui l'applicazione viene visualizzata quando il dispositivo è collegato al computer.

> [!Note]  
> [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) e [System. AppUserModel. RelaunchDisplayNameResource]() devono essere impostati sempre insieme. Se una di queste proprietà non è impostata, non viene usato nessuno dei due.

 

Questa proprietà viene utilizzata solo se una finestra dispone di un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se la finestra non contiene un AppUserModelID esplicito, questa proprietà viene ignorata e la finestra viene raggruppata e bloccata come se facesse parte del processo a cui appartiene. Per ulteriori informazioni sull'applicazione di AppUserModelIDs espliciti e sul relativo effetto sul blocco della barra delle applicazioni, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md). Questa proprietà deve essere usata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite. Per ulteriori informazioni, vedere [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Questa proprietà viene ignorata se si imposta [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) . Questo consente a un'applicazione di controllare il raggruppamento delle relative finestre assegnando loro AppUserModelIDs espliciti ma impedendo l'aggiunta di tali finestre.

 

Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System. AppUserModel. RelaunchDisplayNameResource]() di tale finestra.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
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

 

 
