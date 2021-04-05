---
title: MDMERGE e file di metadati
description: Compone più file di metadati (con estensione winmd) in un numero di file di metadati di output, in base allo spazio dei nomi.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- file WinMD
- Metadati di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955203"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE e file di metadati

Compone più file di metadati (con estensione winmd) in un numero di file di metadati di output, in base allo spazio dei nomi.

## <a name="usage"></a>Utilizzo

Eseguire MDMERGE dalla riga di comando usando il comando seguente:

 *< ***Opzioni*** di Mdmerge>*

dove *<  Options >* rappresenta le opzioni della riga di comando che si desidera utilizzare.

Generare file di metadati per i componenti Windows Runtime personalizzati usando il compilatore MIDLRT. Per altre informazioni, vedere [MIDLRT and Windows Runtime Components](midlrt-and-windows-runtime-components.md).

## <a name="command-line-switches"></a>Opzioni della riga di comando

Nell'elenco seguente vengono illustrate le opzioni della riga di comando utilizzate da MDMERGE.

<dl>

[**/i**](-mdmerge-i.md)  
[**\_dir/Metadata**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Quando si usano i parametri **-h** e **/?** è disponibile un elenco completo delle opzioni e delle opzioni del compilatore MDMERGE. interruttori.

## <a name="remarks"></a>Commenti

La composizione dei metadati consente a più file IDL di contenere definizioni per i componenti Windows Runtime nello stesso spazio dei nomi. Ciò consente di definire tutti i tipi in uno spazio dei nomi all'interno di un singolo file IDL.

È probabile che siano presenti numerosi componenti Windows Runtime usati dalle app. Quando si esegue il passaggio finale per produrre assembly di metadati distribuibile Windows Runtime, è possibile configurare MDMERGE per unire i componenti da più directory di metadati, ad esempio quelli installati con il sistema (% WINDOWS% \\ system32 \\ WinMetadata), i tipi di base e la directory di compilazione del progetto corrente. Tutti i tipi necessari vengono uniti negli assembly di metadati corretti, distribuibile, che è possibile creare in un pacchetto per Windows Store.

È possibile utilizzare l'opzione [**/n**](-mdmerge-n.md) per specificare la profondità dello spazio dei nomi supportata per la composizione degli assembly di metadati. Ciò consente di configurare una suddivisione a caldo per i componenti di Windows Runtime, in modo da creare un pacchetto di un singolo file con estensione WinMD anziché di molti. In questo modo si riducono i tempi di caricamento e I/O dei file richiesti dalle app di Windows Store.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti di MIDLRT e Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




