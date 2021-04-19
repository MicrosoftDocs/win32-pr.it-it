---
description: Vengono descritti i collegamenti reali e le giunzioni.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Collegamenti reali e giunzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317787"
---
# <a name="hard-links-and-junctions"></a>Collegamenti reali e giunzioni

Nel file system NTFS sono supportati tre tipi di collegamenti file: collegamenti reali, giunzioni e collegamenti simbolici. Questo argomento è una panoramica dei collegamenti e delle giunzioni reali. Per informazioni sui collegamenti simbolici, vedere [creazione di collegamenti simbolici](creating-symbolic-links.md).

## <a name="hard-links"></a>Collegamenti reali

Un *collegamento fisso* è la rappresentazione file System di un file in base al quale più di un percorso fa riferimento a un singolo file nello stesso volume. Per creare un collegamento reale, utilizzare la funzione [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) . Tutte le modifiche apportate al file sono immediatamente visibili alle applicazioni che vi accedono tramite i collegamenti reali che vi fanno riferimento. Le informazioni sulle dimensioni e sugli attributi delle voci di directory vengono tuttavia aggiornate solo per il collegamento attraverso il quale è stata apportata la modifica. Si noti che gli attributi del file vengono riflessi in tutti i collegamenti reali a tale file e le modifiche apportate agli attributi di tale file vengono propagate a tutti i collegamenti reali. Se ad esempio si reimposta l'attributo READONLY su un collegamento reale per eliminare quel particolare collegamento e sono presenti più collegamenti reali al file effettivo, sarà necessario reimpostare il bit di sola lettura sul file da uno dei collegamenti reali rimanenti per riportare il file e tutti i collegamenti reali rimanenti allo stato di sola lettura.

Ad esempio, in un sistema in cui C: e D: sono unità locali e Z: è un'unità di rete mappata a \\ \\ Fred \\ share, i riferimenti seguenti sono consentiti come un collegamento fisso:

-   C: \\ dira \\ethel.txt collegato a c: \\ dirB \\ DIRC \\lucy.txt
-   D: \\ dir1 \\tinker.txt a d: \\ dir2 \\ DirX \\bell.txt
-   C: \\ diry \\ Bob. bak collegato a c: \\ dir2 \\mina.txt

Gli elementi seguenti non sono:

-   C: \\ dira collegato a c: \\ dirB
-   C: \\ dira \\ethel.txt collegato a D: \\ dirB \\lucy.txt
-   C: \\ dira \\ethel.txt collegato alla Z: \\ dirB \\lucy.txt

Per eliminare un collegamento reale, utilizzare la funzione [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) . È possibile eliminare i collegamenti reali in qualsiasi ordine indipendentemente dall'ordine in cui vengono creati.

## <a name="junctions"></a>Giunzioni

Una *giunzione* (anche denominata *collegamento flessibile*) differisce da un collegamento reale in quanto gli oggetti di archiviazione a cui fa riferimento sono directory separate e una giunzione può collegare le directory che si trovano in volumi locali diversi nello stesso computer. In caso contrario, le giunzioni operano in modo identico ai collegamenti reali. Le giunzioni vengono implementate tramite [reparse point](reparse-points.md).

Supponendo le stesse condizioni nella sezione dei collegamenti reali, i riferimenti seguenti sono consentiti come giunzioni:

-   C: \\ dira collegato a c: \\ dirB \\ DIRC
-   C: \\ DirX collegato a D: \\ diry

Gli elementi seguenti non sono:

-   C: \\ dira \\one.txt collegato a c: \\ dirB \\two.txt
-   C: \\ dir1 collegato a Z: \\ dir2

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di collegamenti simbolici](creating-symbolic-links.md)
</dt> </dl>

 

 



