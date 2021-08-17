---
description: Applicazioni, processi e finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco MFU (Most Frequently Used) del menu Start.
title: Come escludere elementi dall'aggiunta alla barra delle applicazioni e dagli elenchi recenti/frequenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3adb60353836e436f4327837c30448c7628a435048cc2a41b0464d56341f410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223565"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Come escludere elementi dall'aggiunta alla barra delle applicazioni e dagli elenchi recenti/frequenti

Applicazioni, processi e finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco MFU (Most Frequently Used) del menu **Start.**

## <a name="instructions"></a>Istruzioni


Esistono tre meccanismi per eseguire l'esclusione di elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti:

-   Aggiungere la voce NoStartPage alla registrazione dell'applicazione, come illustrato in questo esempio:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    I dati associati alla voce NoStartPage vengono ignorati. È necessaria solo la presenza della voce. Pertanto, il tipo ideale per NoStartPage è **REG \_ NONE.**

    Si noti che qualsiasi uso di un ID modello utente dell'applicazione esplicito (AppUserModelID) esegue l'override della voce NoStartPage. Se un AppUserModelID esplicito viene applicato a un collegamento, un processo o una finestra, diventa pinnable e idoneo per l'elenco MFU del menu **Start.**

-   Impostare la [proprietà System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) nelle finestre e nei collegamenti. Questa proprietà deve essere impostata in una finestra prima di impostare la [proprietà PKEY \_ AppUserModel \_ ID.](../properties/props-system-appusermodel-id.md)
-   Aggiungere un AppUserModelID esplicito come valore nella sottochiave del Registro di sistema seguente, come illustrato in questo esempio:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Ogni voce è un **valore REG \_ NULL** con il nome di AppUserModelID. Qualsiasi AppUserModelID trovato in questo elenco non è aggiungibile e non è idoneo per l'inclusione nell'elenco MFU del menu **Start.**

## <a name="remarks"></a>Commenti

Tenere presente che alcuni file eseguibili, nonché i collegamenti che contengono determinate stringhe nei nomi, vengono automaticamente esclusi dall'aggiunta e dall'inclusione nell'elenco MFU.

> [!Note]  
> Questa esclusione automatica può essere sostituita applicando un AppUserModelID esplicito.

 

Se una delle stringhe seguenti, indipendentemente dalla distinzione tra maiuscole e minuscole, è inclusa nel nome del collegamento, il programma non è bloccabile e non viene visualizzato nell'elenco usato più di frequente (non applicabile Windows 10):

-   Documentazione
-   Help
-   Installazione
-   Altre informazioni
-   Leggimi
-   Leggi per primo
-   File Leggimi
-   Rimuovi
-   Eseguire la configurazione
-   Supporto
-   Novità

L'elenco di programmi seguente non è modificabile e viene escluso dall'elenco usato più di frequente:

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Gli elenchi precedenti vengono archiviati nei valori del Registro di sistema seguenti.

> [!Note]  
> Questi elenchi non devono essere modificati dalle applicazioni. Usare uno dei metodi dell'elenco di esclusione descritti in precedenza in questo argomento per la stessa esperienza.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra delle applicazioni](taskbar.md)
</dt> <dt>

[Estensioni della barra delle applicazioni](taskbar-extensions.md)
</dt> </dl>

 

 
