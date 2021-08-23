---
title: Registrazione di un servizio
description: Per aggiungere il servizio all'elenco di provider nella Pubblicazione guidata sul Web o nell'Ordinamento guidato stampa online, è necessario aggiungere la chiave appropriata e i relativi valori al Registro di Windows sistema.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrare, servizi
- Pubblicazione guidata sul Web, registrazione
- Online Print Ordering Wizard,registering
- registrazione, Pubblicazione guidata sul Web
- registrazione, Ordinamento guidato stampa online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f5e3f43fe981558fcbf8573eb8768646f112f4816486159cc7c16d71e40e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608641"
---
# <a name="registering-a-service"></a>Registrazione di un servizio

Per aggiungere il servizio all'elenco di provider nella Pubblicazione guidata sul Web o nell'Ordinamento guidato stampa online, è necessario aggiungere la chiave appropriata e i relativi valori al Registro di Windows sistema.

## <a name="required-keys-and-values"></a>Chiavi e valori obbligatori

Per aggiungere il servizio all'elenco di provider per la Pubblicazione guidata sul Web, aggiungere una chiave come illustrato di seguito.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Per aggiungere il servizio all'elenco di provider per l'Ordinamento guidato stampa online, aggiungere una chiave come illustrato di seguito.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Ognuno dei valori è una stringa di tipo REG \_ SZ. Specificare i dati come illustrato nella tabella seguente. 

| Nome del valore     | Spiegazione                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Percorso completo del file dell'icona, incluso il nome del file.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | Nome visualizzato per il servizio nell'elenco dei provider della procedura guidata.                                                                                                                                                                                                                                                                                                                                                             |
| Descrizione    | Breve descrizione del servizio. Questa descrizione viene visualizzata anche nell'elenco dei provider della procedura guidata direttamente sotto il nome del servizio.                                                                                                                                                                                                                                                                                    |
| Href           | URL della prima pagina del servizio.                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipi supportati | Tipi di file supportati dal servizio. Ad esempio, *\*.jpg*. Specificando solo determinati tipi di file, il servizio viene visualizzato solo quando sono stati selezionati tali tipi di file. Se è stato selezionato più di un tipo di file, il servizio viene visualizzato se uno di questi tipi di file è supportato dal servizio. Se si desidera specificare più tipi di file, separarli nell'elenco con punti e virgola. Ad esempio, *\*.jpg; \*.bmp*. |



 

Di seguito è riportato un esempio completo per un servizio di elaborazione foto intitolato "MyProvider".

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

Quando viene chiamato l'URL del servizio, vengono aggiunti due valori alla fine dell'URL: lcid e langid. Ad esempio, la stringa dell'URL per l'esempio precedente potrebbe essere https: \/ /www.MyProvider.com/Intro.htm?lcid=1033&langid=1033. Queste variabili vengono usate per informazioni sulla lingua e sulla localizzazione.

-   **lcid** viene usato per informare il server delle impostazioni relative a paese/area geografica e lingua del client. Non viene usato per determinare la lingua dell'interfaccia utente del client, ma viene usato per determinare il formato corretto per valuta, data e ora e altri dati specifici dell'area.
-   **langid viene** usato per informare il server dell'impostazione della lingua predefinita del client in modo che possa usare la lingua corretta nell'interfaccia utente.

 

 




