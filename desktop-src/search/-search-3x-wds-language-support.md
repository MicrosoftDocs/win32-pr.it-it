---
description: In questo argomento viene descritto come Windows Search supporta più lingue.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Lingue supportate da Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750434"
---
# <a name="languages-supported-by-windows-search"></a>Lingue supportate da Windows Search

In questo argomento viene descritto come Windows Search supporta più lingue.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Token, wordbreaker e risorse della lingua

Windows Search è indipendente dal linguaggio, ma l'accuratezza della ricerca tra i linguaggi può variare a causa del modo in cui Wordbreaker tokenize testo. Wordbreaker implementano varie regole per la suddivisione in token per le lingue e suddividono il testo in singoli token o parole per essere indicizzati o cercati.

Sia il linguaggio del testo indicizzato che la stringa di query vengono suddivisi in token. Poiché le regole di token variano in base al linguaggio, esistono Wordbreaker separate per ogni lingua o famiglia di linguaggi. In caso di mancata corrispondenza tra il linguaggio di query e la lingua indicizzata, i risultati possono essere imprevedibili.

Windows Search viene fornito con un set di Wordbreaker ben definito. I componenti Word breaker e stemmer classici sono supportati in Windows Vista e versioni successive. Se non è possibile determinare la lingua di un documento, la ricerca di Windows tenterà di rilevare la lingua per identificare i Word breaker più appropriati. Windows Search tenta di rilevare la lingua chiamando la funzione [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) per determinare la prima lingua MUI (multiple User Interface), che in genere è la lingua dell'interfaccia utente del sistema, a meno che non siano installati i Language Pack MUI. Se la chiamata ha esito positivo, viene usato Word breaker per la prima lingua MUI. Se la chiamata a **GetSystemPreferredUILanguages** ha esito negativo, Windows Search recupera le impostazioni locali del sistema chiamando la funzione [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) e USA Word breaker associato a tali impostazioni locali.

Se non è installato alcun word breaker per una lingua, Windows Search interrompe lo spazio vuoto usando il Word breaker **neutro** .

È possibile rimuovere una lingua tramite il registro di sistema, come illustrato nell'esempio seguente.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> Se si apportano modifiche al registro di sistema, riavviare Windows Search.

 

Quando la ricerca di Windows richiede un nuovo Word breaker, viene letto l'identificatore di classe (CLSID) e il Word breaker di cui è stata creata un'istanza viene memorizzato nella cache.

È possibile creare un Word breaker personalizzato per un linguaggio implementando l'interfaccia [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) . Windows Search chiama quindi i metodi **IWordBreaker** quando compila gli indici di contenuto ed esegue le query.

Le informazioni sulle impostazioni locali per il contenuto indicizzato vengono recuperate dall'origine del contenuto. Se l'implementatore di origine non conosce le impostazioni locali del contenuto indicizzato, deve impostare le impostazioni locali su [**\_ indipendente dalle impostazioni locali**](../intl/locale-neutral.md).

Se, ad esempio, si implementa un gestore di filtro (un'implementazione dell'interfaccia [**IFilter**](https://www.bing.com/search?q=**IFilter**) ), un gestore di proprietà o un gestore di protocollo, è necessario impostare le impostazioni locali per il contenuto indicizzato su [**\_ Neutral impostazioni locali**](../intl/locale-neutral.md) a meno che non si disponga di informazioni specifiche sulle impostazioni locali e si sia certi della relativa accuratezza.

> [!TIP]
> Se una query sull'indice è basata sull'input dell'utente, le impostazioni locali devono corrispondere alla lingua in cui l'utente sta digitando. È possibile determinare queste impostazioni locali chiamando la funzione [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) .

 

## <a name="languages-supported-by-wordbreakers"></a>Linguaggi supportati da Wordbreaker

Windows Search include Wordbreaker per supportare le lingue seguenti.



| Chiave del Registro di sistema             | Lingua (lingua inglese)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **\_Saudiarabia arabo**  | Arabo (neutro)                                  | 0x0001 |
| **\_Impostazioni predefinite Bengali**     | Bangla (neutro)                                  | 0x0045 |
| **\_Valore predefinito bulgaro**   | Bulgaro (Bulgaria)                              | 0x0402 |
| **\_Valore predefinito catalano**     | Catalano (Catalogna)                                 | 0x0403 |
| **Cinese \_ Hongkong**    | Cinese (Hong Kong - R.A.S., Repubblica popolare cinese)                      | 0x0C04 |
| **Cinese \_ semplificato**  | Cinese (semplificato)                              | 0x0804 |
| **Cinese \_ tradizionale** | Cinese (tradizionale)                             | 0x0404 |
| **\_Valore predefinito croato**    | Croato (Croazia)                                | 0x041A |
| **\_Valore predefinito ceco**       | Ceco (Repubblica Ceca)                            | 0x0405 |
| **\_Impostazione predefinita danese**      | Danese (Danimarca)                                  | 0x0406 |
| **Olandese \_ olandese**         | Olandese (Paesi Bassi)                               | 0x0413 |
| **Inglese ( \_ Regno Unito)**          | Inglese (Regno Unito)                          | 0x0809 |
| **Inglese ( \_ Stati Uniti)**          | Inglese (Stati Uniti)                           | 0x0409 |
| **\_Impostazione predefinita finlandese**     | Finlandese (Finlandia)                                 | 0x040B |
| **Francese \_ francese**       | Francese (Francia)                                   | 0x040C |
| **Tedesco \_ tedesco**       | Tedesco (Germania)                                  | 0x0407 |
| **\_Impostazioni predefinite greche**       | Greco (Grecia)                                    | 0x0408 |
| **\_Predefinito Gujarati**    | Gujarati (India)                                  | 0x0447 |
| **\_Impostazione predefinita ebraica**      | Ebraico (neutro)                                  | 0x000D |
| **\_Impostazione predefinita Hindi**       | Hindi (India)                                     | 0x0439 |
| **\_Valore predefinito ungherese**   | Ungherese (Ungheria)                               | 0x040E |
| **\_Impostazione predefinita islandese**   | Islandese (Islanda)                               | 0x040F |
| **\_Impostazione predefinita indonesiano**  | Indonesiano (Indonesia)                            | 0x0421 |
| **Italiano \_ Italiano**     | Italiano (Italia)                                   | 0x0410 |
| **\_Impostazione predefinita giapponese**    | Giapponese (Giappone)                                  | 0x0411 |
| **\_Impostazione predefinita Kannada**     | Kannada (India)                                   | 0x044B |
| **\_Impostazione predefinita coreano**      | Coreano (Corea)                                    | 0x0412 |
| **\_Valore predefinito lettone**     | Lettone (Lettonia)                                  | 0x0426 |
| **\_Valore predefinito lituano**  | Lituano (Lituano)                           | 0x0427 |
| **Malesia malese \_**      | Malese (Malaysia)                                  | 0x043E |
| **\_Valore predefinito Malayalam**   | Malayalam (neutro)                               | 0x004C |
| **\_Impostazione predefinita Marathi**     | Marathi (India)                                   | 0x044E |
| **\_Bokmal norvegese**    | Norvegese (Bokmål, Norvegia)                        | 0x0414 |
| **\_Predefinito polacco**      | Polacco (Polonia)                                   | 0x0415 |
| **\_Portogallo Portoghese** | Portoghese (Portogallo)                             | 0x0816 |
| **\_Brasile Portoghese**   | Portoghese (Brasile)                               | 0x0416 |
| **\_Impostazione predefinita Punjabi**     | Punjabi (India)                                   | 0x0446 |
| **\_Valore predefinito rumeno**    | Romeno (Romania)                                | 0x0418 |
| **\_Impostazione predefinita russo**     | Russo (neutro)                                 | 0x0019 |
| **Serbo \_ cirillico**    | Serbo (Serbia e Montenegro, precedente, cirillico) | 0x0C1A |
| **Serbo ( \_ alfabeto latino)**       | Serbo (Serbia e Montenegro, ex, alfabeto latino)    | 0x081A |
| **\_Impostazione predefinita slovacco**      | Slovacco (Slovacchia)                                 | 0x041B |
| **\_Impostazione predefinita sloveno**   | Sloveno (Slovenia)                              | 0x0424 |
| **Spagnolo \_ moderno**      | Spagnolo (Spagna, ordinamento moderno)                      | 0x0C0A |
| **\_Impostazione predefinita svedese**     | Svedese (Svezia)                                  | 0x041D |
| **\_Valore predefinito Tamil**       | Tamil (India)                                     | 0x0449 |
| **\_Valore predefinito Telugu**      | Telugu (India)                                    | 0x044A |
| **\_Impostazioni predefinite Thai**        | Thai (Thailandia)                                   | 0x041E |
| **\_Impostazione predefinita turca**     | Turco (Turchia)                                  | 0x041F |
| **Impostazione predefinita per l'ucraino \_**   | Ucraino (Ucraina)                               | 0x0422 |
| **\_Impostazione predefinita Urdu**        | Urdu (Pakistan)                                   | 0x0420 |
| **\_Impostazione predefinita vietnamita**  | Vietnamita (Vietnam)                              | 0x042A |



 

> [!Note]  
> Gli LCID per alcune lingue della tabella vengono generati utilizzando l'identificatore di lingua, l'identificatore del linguaggio e l'identificatore di ordinamento.

 

Per altre informazioni sui linguaggi e gli identificatori associati, vedere [costanti e stringhe degli identificatori di lingua](../intl/language-identifier-constants-and-strings.md).

> [!Note]  
> Non vi è alcuna garanzia che tutte queste chiavi del registro di sistema siano presenti in un determinato computer. Il Word breaker per una determinata lingua può essere installato o meno nel computer a seconda delle impostazioni utente.

 

A **partire da Windows 8.1**, il modo migliore per usare Wordbreaker è tramite la [**classe WordsSegmenter**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)dell'API WinRT.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sull'implementazione e sull'utilizzo di Word breaker e stemmer personalizzati per lingue e impostazioni locali aggiuntive, vedere [estensione delle risorse di lingua in Windows Search](extending-language-resources-in-windows-search.md).
-   Se è necessario identificare la lingua di un testo, è possibile usare il rilevamento automatico del linguaggio (LAD), disponibile in Windows 7 e versioni successive. Per ulteriori informazioni, vedere [servizi linguistici estesi](../intl/extended-linguistic-services.md) (ELS).
-   Per informazioni sulla gestione, sull'esecuzione di query e sull'estensione dell'indice, vedere la guida per gli [sviluppatori di Windows Search](-search-developers-guide-entry-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Uso di codice gestito con i dati della shell e Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
