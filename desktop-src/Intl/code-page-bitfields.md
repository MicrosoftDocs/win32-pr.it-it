---
description: La tabella codici campi viene utilizzata nelle strutture FONTSIGNATURE e LOCALESIGNATURE. Si noti che tutte le impostazioni locali non supportano le tabelle codici.
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: Tabella codici campi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f9df44ac14d935a026a10ab1e71eb7378840de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319987"
---
# <a name="code-page-bitfields"></a>Tabella codici campi

La tabella codici campi viene utilizzata nelle strutture [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) e [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .

> [!Note]  
> Tutte le impostazioni locali non supportano le tabelle codici. I campi descritti in questo argomento non si applicano alle impostazioni locali Unicode. Per determinare gli script supportati per le impostazioni locali, l'applicazione può usare le impostazioni locali costanti dell'identificatore delle impostazioni locali [ \_ SSCRIPTS](locale-sscripts.md) con [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex).

 

> [!Note]  
> La presenza di un bit in una tabella codici bit non significa necessariamente che tutte le stringhe per le impostazioni locali possano essere codificate in tale tabella codici senza perdita. Per mantenere i dati senza perdita, è consigliabile utilizzare Unicode UTF-8 o UTF-16.

 



| bit          | Tabella codici | Descrizione                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | Latino 1                                               |
| 1            | 1250      | Latino 2: Europa centrale                               |
| 2            | 1251      | Cirillico                                              |
| 3            | 1253      | Greco                                                 |
| 4            | 1254      | Turco                                               |
| 5            | 1255      | Ebraico                                                |
| 6            | 1256      | Arabo                                                |
| 7            | 1257      | Baltico                                                |
| 8            | 1258      | Vietnamita                                            |
| 9 - 15       |           | Riservato per ANSI                                     |
| ANSI e OEM |           |                                                       |
| 16           | 874       | Thai                                                  |
| 17           | 932       | Giapponese (Shift-JIS)                                   |
| 18           | 936       | Cinese semplificato (PRC, Singapore)                   |
| 19           | 949       | Codice Hangul unificato coreano (codice Hangul TongHabHyung) |
| 20           | 950       | Cinese tradizionale (Taiwan; RAS di Hong Kong, PRC)      |
| 21           | 1361      | Coreano (Johab)                                        |
| 22 - 29      |           | Riservato per ANSI e OEM alternativi                   |
| 30 - 31      |           | Riservato dal sistema.                                   |
| OEM          |           |                                                       |
| 32-46      |           | Riservato per OEM                                      |
| 47           | 1258      | Vietnamita                                            |
| 48           | 869       | Greco moderno                                          |
| 49           | 866       | Russo                                               |
| 50           | 865       | Area lingue nordiche                                                |
| 51           | 864       | Arabo                                                |
| 52           | 863       | Francese (Canada)                                       |
| 53           | 862       |                                                       |
| 54           | 861       | Islandese                                             |
| 55           | 860       | Portoghese                                            |
| 56           | 857       | Turco                                               |
| 57           | 855       | Cyrillic principalmente russo                           |
| 58           | 852       | Latino 2                                               |
| 59           | 775       | Baltico                                                |
| 60           | 737       | Greco in precedenza 437G                                  |
| 61           | 708; 720  | Arabo ASMO 708                                      |
| 62           | 850       | Latino multilingue 1                                  |
| 63           | 437       | US                                                    |



 

 

 



