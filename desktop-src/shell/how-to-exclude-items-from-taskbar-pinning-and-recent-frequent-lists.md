---
description: Le applicazioni, i processi e le finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco dei menu Start (MFU) usato più di frequente.
title: Come escludere elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979562"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Come escludere elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti

Le applicazioni, i processi e le finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco dei menu **Start** (MFU) usato più di frequente.

## <a name="instructions"></a>Istruzioni


Esistono tre meccanismi per eseguire l'esclusione di elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti:

-   Aggiungere la voce NoStartPage alla registrazione dell'applicazione, come illustrato nell'esempio seguente:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    I dati associati alla voce NoStartPage vengono ignorati. È necessaria solo la presenza della voce. Pertanto, il tipo ideale per NoStartPage è **reg \_ None**.

    Si noti che qualsiasi utilizzo di un ID modello utente applicazione esplicito (AppUserModelID) sostituisce la voce NoStartPage. Se un AppUserModelID esplicito viene applicato a un collegamento, a un processo o a una finestra, diventa aggiungibili e idoneo per l'elenco MFU del menu **Start** .

-   Impostare la proprietà [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) in Windows e i collegamenti. Questa proprietà deve essere impostata su una finestra prima che venga impostata la proprietà [ \_ \_ ID AppUserModel pkey](../properties/props-system-appusermodel-id.md) .
-   Aggiungere un AppUserModelID esplicito come valore nella seguente sottochiave del registro di sistema, come illustrato in questo esempio:

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

    Ogni voce è un valore **reg \_ null** con il nome del AppUserModelID. Qualsiasi AppUserModelID trovato in questo elenco non è aggiungibili e non è idoneo per l'inclusione nell'elenco MFU del menu **Start** .

## <a name="remarks"></a>Commenti

Tenere presente che alcuni file eseguibili, oltre a collegamenti che contengono determinate stringhe nei rispettivi nomi, vengono automaticamente esclusi dal blocco e dall'inclusione nell'elenco MFU.

> [!Note]  
> Questa esclusione automatica può essere sottoposta a override applicando un AppUserModelID esplicito.

 

Se una delle stringhe seguenti, indipendentemente dalla distinzione tra maiuscole e minuscole, è inclusa nel nome del collegamento, il programma non è aggiungibili e non viene visualizzato nell'elenco degli elementi utilizzati più di frequente (non applicabile a Windows 10):

-   Documentazione
-   Help
-   Installazione
-   Altre informazioni
-   Leggi
-   Leggi prima
-   File Leggimi
-   Rimuovi
-   Configurazione
-   Supporto
-   Novità

L'elenco di programmi seguente non è aggiungibili e viene escluso dall'elenco degli elementi utilizzati più di frequente:

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

Gli elenchi precedenti vengono archiviati nei seguenti valori del registro di sistema.

> [!Note]  
> Questi elenchi non devono essere modificati dalle applicazioni. Per la stessa esperienza, utilizzare uno dei metodi dell'elenco di esclusioni descritti in precedenza in questo argomento.

 

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

 

 
