---
description: In questo argomento viene illustrato come registrare un gestore di anteprime associato a un determinato tipo di dati.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Come registrare un gestore di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979519"
---
# <a name="how-to-register-a-preview-handler"></a>Come registrare un gestore di anteprime

In questo argomento viene illustrato come registrare un gestore di anteprime associato a un determinato tipo di dati. Ai fini dell'illustrazione, gli esempi in questo argomento usano un tipo di file xyz. La registrazione di un gestore di anteprime è una registrazione standard basata sull'associazione di file.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Per prima cosa, un'estensione del nome file è associata a un ProgID. La voce seguente associa la sottochiave ProgID **xyzfile** con l'estensione del nome di file xyz.

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

Ogni sottochiave ProgID del gestore di anteprime contiene una sottochiave denominata **ShellEx** che contiene una sottochiave denominata *sempre* **{8895b1c6-b41f-4c1c-a562-0d564250836f}**. La presenza della sottochiave indica al sistema che il gestore è un gestore di anteprime.

Il valore predefinito della sottochiave **{8895b1c6-b41f-4c1c-a562-0d564250836f}** è l'identificatore di classe (CLSID) del gestore. Di seguito è riportato un esempio della sottochiave ProgID **xyzfile** , che associa un gestore di CLSID {ec3a629a-a47c-4245-BC78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Passaggio 2:

Successivamente, aggiungere la sottochiave in **CLSID** per il gestore di anteprime. Un esempio è illustrato di seguito. Segue una spiegazione delle singole voci.

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

Il valore predefinito per la sottochiave (in questo caso, **{ec3a629a-a47c-4245-BC78-b4b63d0e3154}**) non è obbligatorio o utilizzato. Tuttavia, l'impostazione su una stringa non localizzata può consentire di eseguire il debug dei problemi di registrazione.

Il segno meno (-101) nella risorsa. dll nella voce DisplayName esiste per motivi legacy. La voce dell'icona, d'altra parte, non richiede un segno meno.

Il valore AppID fornisce un riferimento all'AppID dell'applicazione associata all'estensione del nome file, archiviata in **HKEY \_ classi \_ radice** \\ **AppID**. Il valore usato qui, {6d2b5079-2f0b-48DD-ab7f-97cec514d30b}, è l'ID dell'host surrogato Prevhost.exe. i gestori di anteprime a 32 bit devono usare **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando vengono installati nei sistemi operativi a 64 bit.

Le voci sotto la sottochiave **InprocServer32** includono un riferimento alla sottochiave ProgID dell'estensione del nome file e una voce per [VersionIndependentProgID](../com/versionindependentprogid.md).

### <a name="step-3"></a>Passaggio 3:

Infine, il gestore di anteprime deve essere aggiunto all'elenco di tutti i gestori di anteprime. Questo elenco viene usato come ottimizzazione dal sistema per enumerare tutti i gestori di anteprime registrati a scopo di visualizzazione. Anche in questo caso, il valore predefinito non è obbligatorio, ma semplicemente il processo di debug.

> [!Note]  
> In Windows 7, se l'applicazione è installata per tutti gli utenti del computer, utilizzare HKEY \_ Local \_ computer; se per un solo utente, utilizzare HKEY \_ Current \_ User.

 

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

[Gestori di anteprime e host di anteprima della shell](preview-handlers.md)
</dt> <dt>

[Compilazione di gestori di anteprime](building-preview-handlers.md)
</dt> <dt>

[Linee guida per il gestore di anteprime](preview-handler-guidelines.md)
</dt> </dl>

 

 
