---
description: Descrive collegamenti rigidi e giunzioni.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Collegamenti rigidi e giunzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ed8b3bbe163d2bad4b8c51715537e194633f02ec200ceb5df02df7d582ae3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107451"
---
# <a name="hard-links-and-junctions"></a>Collegamenti rigidi e giunzioni

Sono supportati tre tipi di collegamenti file nel file system NTFS: collegamenti rigidi, giunzioni e collegamenti simbolici. Questo argomento fornisce una panoramica dei collegamenti rigidi e delle giunzioni. Per informazioni sui collegamenti simbolici, vedere [Creazione di collegamenti simbolici.](creating-symbolic-links.md)

## <a name="hard-links"></a>Collegamenti reali

Un *collegamento rigido* è la file system di un file in base al quale più di un percorso fa riferimento a un singolo file nello stesso volume. Per creare un collegamento rigido, usare [**la funzione CreateHardLink.**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) Tutte le modifiche apportate al file sono immediatamente visibili alle applicazioni che vi accedono tramite i collegamenti rigidi che vi fanno riferimento. Tuttavia, le informazioni sulle dimensioni delle voci di directory e sugli attributi vengono aggiornate solo per il collegamento tramite il quale è stata apportata la modifica. Si noti che gli attributi nel file si riflettono in ogni collegamento rigido a tale file e le modifiche apportate agli attributi del file vengono propagate a tutti i collegamenti rigidi. Ad esempio, se si reimposta l'attributo READONLY su un collegamento rigido per eliminare quel particolare collegamento rigido e sono presenti più collegamenti reali al file effettivo, sarà necessario reimpostare il bit READONLY nel file da uno dei collegamenti reali rimanenti per riportare il file e tutti i collegamenti reali rimanenti allo stato READONLY.

Ad esempio, in un sistema in cui C: e D: sono unità locali e Z: è un'unità di rete mappata a una condivisione di rete, i riferimenti seguenti sono consentiti \\ \\ come collegamento \\ rigido:

-   C: \\ dira \\ethel.txt collegato a C: \\ dirb \\ dirc \\lucy.txt
-   D: \\ dir1 \\tinker.txt a D: \\ dir2 \\ dirx \\bell.txt
-   C: \\ diry \\ bob.bak collegato a C: \\ dir2 \\mina.txt

Le operazioni seguenti non sono:

-   C: \\ dira collegato a C: \\ dirb
-   C: \\ dira \\ethel.txt collegato a D: \\ dirb \\lucy.txt
-   C: \\ dira \\ethel.txt collegato a Z: \\ dirb \\lucy.txt

Per eliminare un collegamento rigido, usare [**la funzione DeleteFile.**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) È possibile eliminare i collegamenti rigidi in qualsiasi ordine, indipendentemente dall'ordine in cui vengono creati.

## <a name="junctions"></a>Giunzioni

Una  giunzione (detta anche collegamento *soft)* differisce da un collegamento rigido in quanto gli oggetti di archiviazione a cui fa riferimento sono directory separate e una giunzione può collegare directory che si trovano in volumi locali diversi nello stesso computer. In caso contrario, le giunzioni funzionano in modo identico ai collegamenti rigidi. Le giunzioni vengono implementate tramite [reparse point.](reparse-points.md)

Supponendo le stesse condizioni nella sezione Collegamenti reali, i riferimenti seguenti sono consentiti come giunzioni:

-   C: \\ dira collegato a C: \\ dirb \\ dirc
-   C: \\ dirx collegato a D: \\ diry

Le operazioni seguenti non sono:

-   C: \\ dira \\one.txt collegato a C: \\ dirb \\two.txt
-   C: \\ dir1 collegato a Z: \\ dir2

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di collegamenti simbolici](creating-symbolic-links.md)
</dt> </dl>

 

 



