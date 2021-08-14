---
description: In questo argomento viene illustrato come registrare un gestore di anteprima associato a un determinato tipo di dati.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Come registrare un gestore di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e1879261750609015acee2ccea1bc6f48f82df78ac7c18cbb2f46fa493c4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223440"
---
# <a name="how-to-register-a-preview-handler"></a>Come registrare un gestore di anteprima

In questo argomento viene illustrato come registrare un gestore di anteprima associato a un determinato tipo di dati. A scopo illustrativo, gli esempi in questo argomento usano un tipo di file con estensione xyz. La registrazione di un gestore di anteprima è una registrazione standard basata sull'associazione di file.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

In primo luogo, un'estensione di file è associata a un ProgID. La voce seguente associa la sottochiave **xyzfile** ProgID all'estensione xyz.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

La sottochiave ProgID **xyzfile** viene archiviata con gli altri ProgID, come illustrato di seguito:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Ogni sottochiave ProgID del gestore di anteprima contiene una  sottochiave denominata **shellex** che contiene sempre una sottochiave denominata **{8895b1c6-b41f-4c1c-a562-0d564250836f}**. La presenza di tale sottochiave indica al sistema che il gestore è un gestore di anteprima.

Il valore predefinito della **sottochiave {8895b1c6-b41f-4c1c-a562-0d564250836f}** è l'identificatore di classe (CLSID) del gestore. Di seguito è riportato un esempio della sottochiave ProgID **xyzfile,** che associa un gestore di CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Passaggio 2:

Aggiungere quindi la sottochiave in **CLSID** per il gestore di anteprima. Di seguito è riportato un esempio. Di seguito viene fornita una spiegazione delle singole voci.

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

Il valore predefinito per la sottochiave (in questo **caso{ ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) non è obbligatorio o usato. Tuttavia, l'impostazione su una stringa non localizzata consente di eseguire il debug dei problemi di registrazione.

Il segno meno (-101) nella risorsa .dll nella voce DisplayName esiste per motivi legacy. La voce Icona, d'altra parte, non richiede un segno meno.

Il valore AppID fornisce un riferimento all'AppID dell'applicazione associata all'estensione del nome file (archiviato in **HKEY \_ CLASSES \_ ROOT** \\ **APPID**. Il valore usato qui, {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}, è l'ID dell'host surrogato Prevhost.exe. I gestori di anteprima a 32 bit devono usare **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} se installati in sistemi operativi a 64 bit.

Le voci nella sottochiave **InprocServer32** includono un riferimento alla sottochiave ProgID dell'estensione di file, nonché una voce per [versionIndependentProgID](../com/versionindependentprogid.md).

### <a name="step-3"></a>Passaggio 3:

Infine, il gestore di anteprima deve essere aggiunto all'elenco di tutti i gestori di anteprima. Questo elenco viene usato come ottimizzazione dal sistema per enumerare tutti i gestori di anteprima registrati a scopo di visualizzazione. Anche in questo caso, il valore predefinito non è obbligatorio, ma è sufficiente per il processo di debug.

> [!Note]  
> In Windows 7, se l'applicazione è installata per tutti gli utenti del computer, usare HKEY LOCAL MACHINE. Se per un solo \_ \_ utente, usare HKEY \_ CURRENT \_ USER.

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprima e host di anteprima della shell](preview-handlers.md)
</dt> <dt>

[Compilazione di gestori di anteprima](building-preview-handlers.md)
</dt> <dt>

[Linee guida per i gestori di anteprima](preview-handler-guidelines.md)
</dt> </dl>

 

 
