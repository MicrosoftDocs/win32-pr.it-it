---
title: Registrazione di un servizio
description: Per aggiungere il servizio all'elenco dei provider tramite la pubblicazione guidata sul Web o la procedura guidata per l'ordine di stampa online, è necessario aggiungere la chiave e i relativi valori appropriati al registro di sistema di Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrazione, servizi
- Pubblicazione guidata sul Web, registrazione
- Procedura guidata per l'ordine di stampa online, registrazione
- registrazione, pubblicazione guidata sul Web
- registrazione, ordinamento guidato stampa online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234911"
---
# <a name="registering-a-service"></a>Registrazione di un servizio

Per aggiungere il servizio all'elenco dei provider tramite la pubblicazione guidata sul Web o la procedura guidata per l'ordine di stampa online, è necessario aggiungere la chiave e i relativi valori appropriati al registro di sistema di Windows.

## <a name="required-keys-and-values"></a>Chiavi e valori obbligatori

Per aggiungere il servizio all'elenco dei provider per la pubblicazione guidata sul Web, aggiungere una chiave come illustrato di seguito.

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

Per aggiungere il servizio all'elenco dei provider per la procedura guidata per l'ordine di stampa online, aggiungere una chiave come illustrato di seguito.

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

Ognuno dei valori è una stringa di tipo REG \_ SZ. Fornire i dati come illustrato nella tabella seguente. 

| Nome del valore     | Spiegazione                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Percorso completo del file di icona, incluso il nome del file.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | Nome visualizzato per il servizio nell'elenco dei provider della procedura guidata.                                                                                                                                                                                                                                                                                                                                                             |
| Descrizione    | Breve descrizione del servizio. Questa descrizione viene visualizzata anche nell'elenco dei provider della procedura guidata direttamente sotto il nome del servizio.                                                                                                                                                                                                                                                                                    |
| HREF           | URL della prima pagina del servizio.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Tipi di file supportati dal servizio. Ad esempio, *\* jpg*. Specificando solo determinati tipi di file, il servizio viene visualizzato solo quando questi tipi di file sono stati selezionati. Se è stato selezionato più di un tipo di file, il servizio viene visualizzato se uno di questi tipi di file è supportato dal servizio. Se si desidera specificare più tipi di file, separarli nell'elenco con un punto e virgola. Ad esempio, *\* . jpg; \* . BMP*. |



 

Di seguito è riportato un esempio completo per un servizio di elaborazione foto denominato "provider".

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

Quando viene chiamato l'URL del servizio, vengono aggiunti due valori alla fine dell'URL, ovvero LCID e langid. Ad esempio, la stringa URL per l'esempio precedente potrebbe essere https: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&LangID = 1033. Queste variabili vengono usate per le informazioni relative alla lingua e alla localizzazione.

-   **LCID** viene usato per informare il server delle impostazioni relative al paese e alla lingua del client. Non viene usato per determinare la lingua dell'interfaccia utente del client, ma viene usato per determinare il formato corretto per valuta, data e ora e altri dati specifici dell'area.
-   **LangID** viene usato per informare il server dell'impostazione della lingua predefinita del client in modo da poter usare la lingua corretta nell'interfaccia utente.

 

 




