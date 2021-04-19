---
description: La tabella della classe contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto. Ogni riga può generare un set di chiavi e valori del registro di sistema. Le informazioni sul ProgId associate sono incluse in questa tabella.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabella classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310982"
---
# <a name="class-table"></a>Tabella classi

La tabella della classe contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto. Ogni riga può generare un set di chiavi e valori del registro di sistema. Le informazioni sul ProgId associate sono incluse in questa tabella.

La tabella della classe contiene le colonne seguenti.



| Colonna           | Tipo                         | Chiave | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | S   | N        |
| Context          | [Identificatore](identifier.md) | S   | N        |
| Componente\_      | [Identificatore](identifier.md) | S   | N        |
| \_Valore predefinito ProgID  | [Text](text.md)             | N   | S        |
| Descrizione      | [Text](text.md)             | N   | S        |
| AppId\_          | [GUID](guid.md)             | N   | S        |
| FileTypeMask     | [Text](text.md)             | N   | S        |
| Icona\_           | [Identificatore](identifier.md) | N   | S        |
| IconIndex        | [Integer](integer.md)       | N   | S        |
| DefInprocHandler | [Filename](filename.md)     | N   | S        |
| Argomento         | [Formattato](formatted.md)   | N   | S        |
| Funzionalità\_        | [Identificatore](identifier.md) | N   | N        |
| Attributi       | [Integer](integer.md)       | N   | S        |



 

## <a name="column-information"></a>Informazioni sulle colonne

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Identificatore di classe (ID) di un server COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contesto
</dt> <dd>

Contesto server per questo server. Immettere uno dei valori seguenti per la chiave CLSID.



| CHIAVE CLSID                             | Descrizione                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Specifica il percorso completo di un'applicazione server locale a 16 bit.             |
| [LocalServer32](../com/localserver32.md)   | Specifica il percorso completo di un'applicazione server locale a 32 bit.             |
| [InprocServer](../com/inprocserver.md)     | Specifica il percorso di una DLL del server in-process.                           |
| [InprocServer32](../com/inprocserver32.md) | Specifica il percorso di un server in-process a 32 bit e il modello di Threading. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella [tabella dei componenti](component-table.md) che specifica il componente il cui file di chiave fornisce il server com.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>\_Valore predefinito ProgID
</dt> <dd>

ID di programma predefinito associato a questo ID di classe. Questa colonna è una chiave esterna nella [tabella ProgId](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzata associata all'ID della classe e all'ID del programma.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_
</dt> <dd>

ID applicazione contenente le informazioni DCOM per l'applicazione associata ( [GUID](guid.md)della stringa). Questa colonna è una chiave esterna nella [tabella AppID](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contiene informazioni per la chiave HKCR (questo CLSID).

Se esistono più modelli, questi devono essere delimitati da un punto e virgola e vengono generate sottochiavi numeriche: 0, 1, 2... Per ulteriori informazioni su questa funzionalità, vedere [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_
</dt> <dd>

Il file che fornisce l'icona associata a questo CLSID. Il programma di installazione scrive la voce in questa colonna sotto la chiave DefaultIcon associata a ProgId. Se non è null, la colonna è una chiave esterna nella tabella delle [Icone](icon-table.md). Se è null, il server COM fornisce la risorsa icona. Le associazioni di file annunciati e i collegamenti richiedono un valore non null in questa colonna per la visualizzazione corretta.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Icona index nel file icona. Può essere Null.

Solo numeri non negativi.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Questo campo specifica il gestore predefinito in-process per il contesto server specificato nel campo di contesto.

Questo campo deve essere null se nel campo di contesto viene visualizzata una chiave CLSID InprocServer o InprocServer.

Se viene visualizzata una chiave CLSID LocalServer o LocalServer32 nel campo contesto, il valore nel campo DefInprocHandler identifica il gestore predefinito in-process.



| Valore                | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valore non numerico    | Il programma di installazione considera un valore non numerico nel campo DefInprocHandler come un file di sistema che funge da gestore in-process a 32 bit specificato dalla chiave InprocHandler32.                                                                                                            |
| Null                 | I campi DefInprocHandler e argument possono essere entrambi null per una chiave CLSID LocalServer o LocalServer32.                                                                                                                                                                           |
| 1 = valore predefinito (sistema) | Il valore predefinito è il gestore in-process a 16 bit specificato da InprocHandler. In questo caso, il valore di InprocHandler è il nome nel registro di sistema in cui è archiviato il valore del gestore predefinito in-process. Ad esempio, HKEY \_ \_ \\ le classi software del computer locale \\ \\ CLSID.     |
| 2 = valore predefinito (sistema) | Il valore predefinito è il gestore in-process a 32 bit specificato da InprocHandler32. In questo caso, il valore di InprocHandler32 è il nome nel registro di sistema in cui è archiviato il valore del gestore predefinito in-process. Ad esempio, HKEY \_ \_ \\ le classi software del computer locale \\ \\ CLSID. |
| 3 = valore predefinito (sistema) | Il valore predefinito è un gestore in-process a 16 bit o a 32 bit.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento
</dt> <dd>

Se viene visualizzata una chiave CLSID LocalServer o LocalServer32 nel campo contesto, il testo in questo campo viene registrato come argomento nel server e viene utilizzato da COM per richiamare il server. I campi DefInprocHandler e argument possono essere entrambi null se LocalServer o LocalServer32 vengono visualizzati nel campo di contesto.

Si noti che la risoluzione delle proprietà nel campo argument è limitata. Una proprietà formattata come \[ proprietà \] in questo campo può essere risolta solo se la proprietà dispone già del valore previsto quando viene installato il componente proprietario della classe. Per l'argomento "MyDoc.doc", ad esempio, per \[ \# \] risolvere il valore corretto, è necessario che lo stesso processo stia installando il file MyDoc.doc e il componente proprietario della classe.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella [tabella delle funzionalità](feature-table.md) che specifica la funzionalità che fornisce il server com.

Chiave esterna per la colonna uno della tabella delle funzionalità.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Se in questa colonna è impostato **msidbClassAttributesRelativePath** , il nome del file Bare può essere utilizzato per i server com. Il programma di installazione registra solo il nome del file anziché il percorso completo. In questo modo il server nella directory corrente avrà la precedenza e consentirà più copie dello stesso componente.



| Attributo                            | Decimal | Valore esadecimale |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l'azione [registerClassInfo](registerclassinfo-action.md) o [UnregisterClassInfo](unregisterclassinfo-action.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
