---
description: Specifica l'icona usata per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o avviare una nuova istanza tramite il relativo pulsante Jump List.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System.AppUserModel.RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970840"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System.AppUserModel.RelaunchIconResource

Specifica l'icona usata per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o avviare una nuova istanza tramite il relativo pulsante Jump List. Si tratta dell'icona usata per il gruppo della barra delle applicazioni e viene visualizzata per un'applicazione aggiunta indipendentemente dal fatto che l'applicazione sia in esecuzione o meno. Deve essere specificato in uno dei formati seguenti:

-   Formato di risorsa standard, ad esempio "%systemdir% \\ system32 \\shell32.dll,-128". Il carattere "-" prima dell'ID risorsa è obbligatorio. Non usare il carattere "@" all'inizio della stringa di percorso.
-   Percorso diretto di un file di icona, ad esempio "%programfiles% \\ Microsoft \\ Blocco note \\ Blocco note.ico,0". Si noti che poiché i file con estensione ico possono contenere più risorse icona, nella stringa è necessario un ID risorsa. Se il file con estensione ico è una singola immagine, usare "0" (senza il carattere "-") come ID risorsa.

[System.AppUserModel.RelaunchIconResource]() è una proprietà facoltativa. Se non è impostata, viene usata l'icona della destinazione del comando di riavvio ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)). Tuttavia, poiché ciò può causare risultati indesiderati, è consigliabile fornire un'icona in modo esplicito tramite questa proprietà.

Questa proprietà viene usata solo se una finestra ha un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se la finestra non ha un AppUserModelID (System.AppUserModel.ID) esplicito, questa proprietà viene ignorata e la finestra viene raggruppata e bloccata come se fosse parte del processo proprietario. Per altre informazioni sull'applicazione di AppUserModelIDs espliciti e sul relativo effetto sull'aggiunta della barra delle applicazioni, vedere ID modello utente applicazione [(AppUserModelIDs).](../shell/appids.md) Questa proprietà deve essere utilizzata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite. Per altre informazioni, vedere [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

Se nella finestra è impostato un AppUserModelID esplicito, ma questa proprietà non è impostata, il sistema tenta di trovare un collegamento con lo stesso AppUserModelID e aggiunge tale collegamento alla barra delle applicazioni per rappresentare la finestra. Se non è possibile trovare tale collegamento, viene usato l'eseguibile di backup del processo proprietario.

> [!Note]  
> Questa proprietà viene ignorata [se System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) è impostato. In questo modo un'applicazione può controllare il raggruppamento delle finestre assegnando loro appUserModelID espliciti, impedendo però che tali finestre vengano bloccate.

 

Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System.AppUserModel.RelaunchIconResource]() di tale finestra.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

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

 

 
