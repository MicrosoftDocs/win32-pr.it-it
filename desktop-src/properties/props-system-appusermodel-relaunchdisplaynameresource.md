---
description: Specifica il nome visualizzato usato per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o avviare una nuova istanza tramite la barra delle applicazioni del Jump List.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System.AppUserModel.RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b0af752fb345dd5dd5f1b091a22255e856031affaca266ff6307045f148cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233023"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System.AppUserModel.RelaunchDisplayNameResource

Specifica il nome visualizzato usato per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o avviare una nuova istanza tramite la barra delle applicazioni del Jump List. Il valore di questa proprietà deve essere uno dei seguenti:

-   Stringa di risorsa indiretta, ad esempio "@%systemdir% \\ system32 \\shell32.dll,-19263". Si noti che il carattere '@' è necessario per distinguere una stringa indiretta da una stringa di testo normale (descritta nel paragrafo puntato successivo). Questa stringa indiretta è costituita da un file binario e da un ID risorsa della stringa contenuta in tale file binario. È consigliabile usare questo formato di stringa indiretta, che garantisce che il nome visualizzato cambi in modo appropriato quando la lingua del sistema viene modificata tramite interfaccia utente multilingue (MUI). Il carattere '-' prima dell'ID risorsa è obbligatorio.
-   Stringa di testo normale che non punta a una risorsa. Deve essere usato solo quando il nome visualizzato viene calcolato in modo dinamico o ottenuto da un'origine dati che non supporta MUI. Ad esempio, la stringa potrebbe essere il nome di un dispositivo, ad esempio "Microsoft Zune", nei casi in cui l'applicazione viene visualizzata quando tale dispositivo è collegato al computer.

> [!Note]  
> [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) e [System.AppUserModel.RelaunchDisplayNameResource]() devono sempre essere impostati insieme. Se una di queste proprietà non è impostata, non viene usata nessuna delle due proprietà.

 

Questa proprietà viene usata solo se una finestra ha un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se la finestra non ha un AppUserModelID esplicito, questa proprietà viene ignorata e la finestra viene raggruppata e bloccata come se fosse parte del processo che la possiede. Per altre informazioni sull'applicazione di AppUserModelID espliciti e sul relativo effetto sul blocco della barra delle applicazioni, vedere ID modello utente applicazione [(AppUserModelIDs).](../shell/appids.md) Questa proprietà deve essere usata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite. Per altre informazioni, vedere [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Questa proprietà viene ignorata [se System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) è impostato. In questo modo un'applicazione può controllare il raggruppamento delle finestre assegnando loro appusermodelID espliciti, ma impedendo che tali finestre vengano bloccate.

 

Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System.AppUserModel.RelaunchDisplayNameResource]() di tale finestra.

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

I valori PKEY sono definiti in Propkey.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelID)](../shell/appids.md)
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

 

 
