---
description: Nell'esempio seguente un'ipotetica società di sviluppo software denominata Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Esempio di associazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad24c3e65ca5b297412c4a69702987cd86b5187dab63dd81435d50e7d06721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009531"
---
# <a name="file-association-example"></a>Esempio di associazione di file

Nell'esempio seguente un'ipotetica società di sviluppo software denominata Litware, Inc. crea un nuovo lettore audio denominato LitwarePlayer. Litware vuole progettare un'associazione di file tra LitwarePlayer e il relativo tipo di file primario, che usa un formato audio appena sviluppato che consente di archiviare un intero CD audio in meno di 10 kilobyte di memoria senza perdita di qualità.

> [!IMPORTANT]
> Questo argomento non si applica a Windows 10. Il funzionamento delle associazioni di file predefinite è stato modificato in Windows 10. Per altre informazioni, vedere la sezione Modifiche al modo in cui Windows 10 **le app predefinite** in questo [post.](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

## <a name="designing-a-new-file-association"></a>Progettazione di una nuova associazione di file

L'azienda deve seguire questa procedura.

1.  **Decidere se il nuovo tipo di file deve essere considerato pubblico o privato.** Questo nuovo tipo di file è un tipo di supporto. Poiché gli utenti scambiano file multimediali tra diverse piattaforme e potrebbero essere presenti altre applicazioni che devono leggere il formato LitwarePlayer, un tipo [di](fa-file-types.md) file pubblico è il più appropriato.
2.  **Determinare se questo tipo di file è già definito.** Controllare il database MIME IANA (Internet Assigned Numbers Authority) e altri database di tipi di file pubblici su Internet per determinare che non è stato definito alcun tipo di file confrontabile. Poiché si tratta di un nuovo formato di file, è necessario definire un nuovo tipo di file.
3.  **Definire un'estensione di file per il nuovo tipo di file.** Gli sviluppatori scelgono , che incorpora l'abbreviazione del fornitore e `.opa-ltw-audio` un suggerimento sul contenuto del file. La ricerca determina che l'estensione non viene usata da altri utenti. In base alle raccomandazioni correnti, non viene definita alcuna estensione breve.
4.  **Definire un tipo MIME per il tipo di file e registrarlo con IANA.** Litware definisce il nuovo tipo MIME come *audio/LitwarePlayer.1* e prepara un'applicazione di tipo MIME, seguendo le linee guida illustrate nei numeri RFC 2045, 2046, 2047 e 2048. Inviano quindi l'applicazione all'IANA, che aggiunge il nuovo tipo di file al database di tipi MIME registrati.
5.  **Determinare se esiste un ProgID per il tipo di file.** Poiché si tratta di un nuovo tipo di file, non esiste [alcun ProgID.](fa-progids.md) Litware imposta sulla progettazione di un nuovo ProgID per LitwarePlayer. Decidono il nome descrittivo "LitwarePlayer Audio Player" (archiviato come risorsa nel file LitwarePlayer.exe) e progettano un'icona predefinita da usare per i file associati a LitwarePlayer (archiviati anche in LitwarePlayer.exe). Poiché LitwarePlayer è una nuova applicazione, si tratta di un ProgID versione 1.
6.  **Registrare progID.** Quando LitwarePlayer è installato, il programma di installazione crea la voce [ProgID](fa-progids.md) seguente nel Registro di sistema.

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    Nella chiave di comando % 1 viene passato come percorso del file da riprodurre.

7.  **Registrare l'estensione del nome file per il tipo di file.** Quando LitwarePlayer è installato, il programma di installazione crea le voci seguenti nel Registro di sistema per l'estensione del tipo di file personalizzata.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Ogni volta che viene creata o modificata un'associazione di file, notificare al sistema che è stata apportata una modifica chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l'evento SHCNE \_ ASSOCCHANGED. Se questa operazione non viene eseguita, shell potrebbe non riconoscere le modifiche apportate fino al riavvio del sistema.

 

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Introduzione alle associazioni di file](fa-intro.md)
-   [Come registrare un browser Internet o un client di posta elettronica con il Windows Start](start-menu-reg.md)
-   [Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Linee guida per la gestione delle applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
