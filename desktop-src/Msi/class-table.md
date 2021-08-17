---
description: La tabella Class contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto. Ogni riga può generare un set di chiavi e valori del Registro di sistema. Le informazioni ProgId associate sono incluse in questa tabella.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabella di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48985bd2d7e9670c89df53993e7170dc3e0e43a2b6e60f63d29e9f43e8d2ab3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066041"
---
# <a name="class-table"></a>Tabella di classi

La tabella Class contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto. Ogni riga può generare un set di chiavi e valori del Registro di sistema. Le informazioni ProgId associate sono incluse in questa tabella.

La tabella Class include le colonne seguenti.



| Colonna           | Tipo                         | Chiave | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | S   | N        |
| Contesto          | [Identificatore](identifier.md) | S   | N        |
| Componente\_      | [Identificatore](identifier.md) | S   | N        |
| Valore predefinito di ProgId \_  | [Text](text.md)             | N   | S        |
| Descrizione      | [Text](text.md)             | N   | S        |
| Appid\_          | [GUID](guid.md)             | N   | S        |
| FileTypeMask     | [Text](text.md)             | N   | S        |
| Icona\_           | [Identificatore](identifier.md) | N   | S        |
| IconIndex        | [Integer](integer.md)       | N   | S        |
| DefInprocHandler | [Filename](filename.md)     | N   | S        |
| Argomento         | [Formattato](formatted.md)   | N   | S        |
| Funzionalità\_        | [Identificatore](identifier.md) | N   | N        |
| Attributi       | [Integer](integer.md)       | N   | S        |



 

## <a name="column-information"></a>Informazioni sulle colonne

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>Clsid
</dt> <dd>

Identificatore di classe (ID) di un server COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contesto
</dt> <dd>

Contesto del server per questo server. Immettere uno dei valori seguenti per la chiave CLSID.



| CHIAVE CLSID                             | Descrizione                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Specifica il percorso completo di un'applicazione server locale a 16 bit.             |
| [LocalServer32](../com/localserver32.md)   | Specifica il percorso completo di un'applicazione server locale a 32 bit.             |
| [InprocServer](../com/inprocserver.md)     | Specifica il percorso di una DLL del server in-process.                           |
| [InprocServer32](../com/inprocserver32.md) | Specifica il percorso di un server in-process a 32 bit e il modello di threading. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella [tabella Component che](component-table.md) specifica il componente il cui file di chiave fornisce il server COM.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>Valore predefinito di ProgId \_
</dt> <dd>

ID programma predefinito associato a questo ID classe. Questa colonna è una chiave esterna nella [tabella ProgID](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzata associata all'ID classe e all'ID programma.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>Appid\_
</dt> <dd>

ID applicazione contenente informazioni DCOM per l'applicazione associata [(GUID stringa](guid.md)). Questa colonna è una chiave esterna nella [tabella AppId](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contiene informazioni per la chiave HKCR (questo CLSID).

Se esistono più modelli, devono essere delimitati da un punto e virgola e vengono generate sottochiavi numeriche: 0, 1, 2... Per altre informazioni su questa funzionalità, vedere [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_
</dt> <dd>

File che fornisce l'icona associata a questo CLSID. Il programma di installazione scrive la voce in questa colonna nella chiave DefaultIcon associata a ProgId. Se non è Null, la colonna è una chiave esterna nella [tabella Icon](icon-table.md). Se è Null, il server COM fornisce la risorsa icona. Le associazioni di file annunciate e i collegamenti richiedono un valore non Null in questa colonna per la corretta visualizzazione.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Indice dell'icona nel file dell'icona. Può essere Null.

Solo numeri non negativi.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Questo campo specifica il gestore in-process predefinito per il contesto del server specificato nel campo Contesto.

Questo campo deve essere Null se nel campo Contesto viene visualizzata una chiave CLSID InprocServer o InprocServer.

Se nel campo Contesto viene visualizzata una chiave CLSID LocalServer o LocalServer32, il valore nel campo DefInprocHandler identifica il gestore in-process predefinito.



| Valore                | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valore non numerico    | Il programma di installazione considera un valore non numerico nel campo DefInprocHandler come file di sistema che funge da gestore in-process a 32 bit specificato dalla chiave InprocHandler32.                                                                                                            |
| Null                 | I campi DefInprocHandler e Argument possono essere entrambi Null per una chiave CLSID LocalServer o LocalServer32.                                                                                                                                                                           |
| 1 = predefinito (sistema) | Il valore predefinito è il gestore in-process a 16 bit specificato da InprocHandler. In questo caso, il valore di InprocHandler è il nome nel Registro di sistema in cui è archiviato il valore del gestore in-process predefinito. Ad esempio, HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID.     |
| 2 = predefinito (sistema) | Il valore predefinito è il gestore in-process a 32 bit specificato da InprocHandler32. In questo caso, il valore di InprocHandler32 è il nome nel Registro di sistema in cui è archiviato il valore del gestore in-process predefinito. Ad esempio, HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID. |
| 3 = predefinito (sistema) | Il valore predefinito è un gestore in-process a 16 o 32 bit.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>discussione
</dt> <dd>

Se nel campo Contesto viene visualizzata una chiave CLSID LocalServer o LocalServer32, il testo in questo campo viene registrato come argomento sul server e viene usato da COM per richiamare il server. I campi DefInprocHandler e Argument possono essere entrambi Null se LocalServer o LocalServer32 viene visualizzato nel campo Contesto.

Si noti che la risoluzione delle proprietà nel campo Argomento è limitata. Una proprietà formattata come Proprietà in questo campo può essere risolta solo se la proprietà ha già il valore previsto quando viene installato il componente proprietario \[ \] della classe. Ad esempio, per risolvere l'argomento "MyDoc.doc" nel valore corretto, lo stesso processo deve installare il file MyDoc.doc e il componente proprietario \[ \# \] della classe.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella [tabella Funzionalità che](feature-table.md) specifica la funzionalità che fornisce il server COM.

Chiave esterna alla colonna uno della tabella Feature.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Se **msidbClassAttributesRelativePath** è impostato in questa colonna, è possibile usare il nome file bare per i server COM. Il programma di installazione registra il nome del file solo anziché il percorso completo. In questo modo il server nella directory corrente ha la precedenza e consente più copie dello stesso componente.



| Attributo                            | Decimal | Valore esadecimale |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene indicata quando viene eseguita [l'azione RegisterClassInfo](registerclassinfo-action.md) o [UnregisterClassInfo.](unregisterclassinfo-action.md)

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

 

 
