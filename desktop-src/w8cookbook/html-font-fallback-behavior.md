---
title: Comportamento del fallback del tipo di carattere HTML
description: Comportamento del fallback del tipo di carattere HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300606"
---
# <a name="html-font-fallback-behavior"></a>Comportamento del fallback del tipo di carattere HTML

## <a name="platform"></a>Piattaforma

Client-* * Windows 8.1  
**Server-** Windows Server 2012 R2  


## <a name="description"></a>Descrizione

Microsoft sta aggiornando la logica per i tipi di carattere dell'interfaccia utente per diverse lingue nelle app di Windows Store tramite HTML. Invece di usare un solo tipo di carattere per tutte le lingue, il tipo di carattere dell'interfaccia utente ora verrà determinato in base al linguaggio. Ad esempio, i tipi di carattere dell'interfaccia utente per il giapponese saranno ora Meiryo interfaccia utente nelle app che usano HTML.

## <a name="manifestation"></a>Manifestazione

Le app che dipendono da un tipo di carattere precedente potrebbero essere diverse; anche se l'aspetto dell'app viene migliorato in generale grazie a tipi di carattere più leggibili, è possibile che si verifichi un problema con i layout che dipendono dalle dimensioni del contenuto in pixel perfetti. Ad esempio, alcune righe di contenuto possono essere più grandi di quelle precedentemente, causando interruzioni di riga e/o il ridimensionamento di elementi contenitore imprevisti. In pratica, tuttavia, non sono stati riscontrati problemi con le app esistenti.

## <a name="solution"></a>Soluzione

Le app interessate possono attenuare questo comportamento specificando un tipo di carattere specifico tramite CSS (ad esempio, "font-family: Meiryo UI") invece di basarsi sui tipi di carattere predefiniti precedenti. La tabella seguente fornisce il tipo di carattere dell'interfaccia utente per ogni nome di script.



| Nome script        | Tipo di carattere dell'interfaccia utente               |
|--------------------|-----------------------|
| Arabo             | Segoe UI              |
| Armeno           | Segoe UI              |
| Bengalese            | Nirmala UI            |
| Bopomofo           | Microsoft JhengHei UI |
| Braille            | Segoe UI Symbol       |
| Buginese           | Leelawadee UI         |
| Sillabico canadese | Gadugi                |
| Cherokee           | Gadugi                |
| Copto             | Segoe UI Symbol       |
| Han (semplificato)   | Microsoft YaHei UI    |
| Han (tradizionale)  | Microsoft JhengHei UI |
| Cirillico           | Segoe UI              |
| Devanagari         | Nirmala UI            |
| Deseret            | Segoe UI Symbol       |
| Etiope           | Ebrima                |
| Georgiano           | Segoe UI              |
| Glagolitico         | Segoe UI Symbol       |
| Gothic             | Segoe UI Symbol       |
| Greco              | Segoe UI              |
| Gujarati           | Nirmala UI            |
| Gurmukhi           | Nirmala UI            |
| Ebraico             | Segoe UI              |
| Corsivo precedente         | Segoe UI Symbol       |
| Giavanese           | Testo giavanese         |
| Giapponese           | Interfaccia utente di Meiryo             |
| Kannada            | Interfaccia utente di Mirmala            |
| Khmer              | Leelawadee UI         |
| Coreano             | Malgun Gothic         |
| Lao                | Leelawadee            |
| Latino              | Segoe UI              |
| Malayalam          | Nirmala UI            |
| Mongolo          | Mongolian Baiti       |
| Myanmar            | Myanmar Text          |
| Modellazione N'Ko               | Ebrima                |
| Ogamico              | Segoe UI Symbol       |
| Chiki OL           | Nirmala UI            |
| Vecchio turco         | Segoe UI Symbol       |
| Oriya              | Nirmala UI            |
| Osmanya            | Ebrima                |
| Carattere phags-pa           | Microsoft PhagsPa     |
| Runico              | Segoe UI Symbol       |
| Sora Sompeng       | Nirmala UI            |
| Singalese            | Nirmala UI            |
| Siriaco             | Estrangelo Edessa     |
| Tai le             | Microsoft Tai Le      |
| Nuovo tai lue        | Microsoft New Tai Lue |
| Tamil              | Nirmala UI            |
| Telugu             | Nirmala UI            |
| Tifinagh           | Ebrima                |
| Thaana             | MV Boli               |
| Thai               | Leelawadee UI         |
| Tibetano            | Microsoft Himalaya    |
| Vai                | Ebrima                |
| Yi                 | Microsoft Yi Baiti    |



 

 

 




