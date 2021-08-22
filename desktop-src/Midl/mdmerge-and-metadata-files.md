---
title: MDMERGE e file di metadati
description: Compone più file di metadati (con estensione winmd) in diversi file di metadati di output, in base allo spazio dei nomi.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- file winmd
- Metadati di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a065a8ff93485728b1c5c4c0c7b43de88e3844a8a013f07caee8d85d76d721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252431"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE e file di metadati

Compone più file di metadati (con estensione winmd) in diversi file di metadati di output, in base allo spazio dei nomi.

## <a name="usage"></a>Uso

Eseguire MDMERGE dalla riga di comando usando il comando seguente:

**mdmerge**  *<* **opzioni**_>_

dove *<***rappresenta** le opzioni della riga di _>_ comando da usare.

Generare i file di metadati per i componenti Windows Runtime personalizzati usando il compilatore MIDLRT. Per altre informazioni, vedere [MIDLRT e Windows Runtime.](midlrt-and-windows-runtime-components.md)

## <a name="command-line-switches"></a>Opzioni della riga di comando

L'elenco seguente mostra le opzioni della riga di comando utilizzate da MDMERGE.

<dl>

[**/i**](-mdmerge-i.md)  
[**/metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Un elenco completo delle opzioni e delle opzioni del compilatore MDMERGE è disponibile quando si usano **-h** e **/?** Interruttori.

## <a name="remarks"></a>Commenti

La composizione dei metadati consente a più file IDL di contenere definizioni Windows componenti runtime nello stesso spazio dei nomi. In questo modo è possibile definire tutti i tipi in uno spazio dei nomi all'interno di un singolo file IDL.

È probabile che siano disponibili numerosi componenti Windows Runtime che le app usano. Quando si esegue il passaggio finale per produrre assembly di metadati Windows Runtime distribuibili, è possibile configurare MDMERGE per unire i componenti da più directory di metadati, ad esempio quelli installati con il sistema (%WINDOWS% \\ system32 WinMetadata), i tipi di base e la directory di compilazione del progetto \\ corrente. Tutti i tipi necessari vengono uniti negli assembly di metadati corretti, distribuibili, che è possibile creare un pacchetto per l Windows Store.

È possibile usare [**l'opzione /n**](-mdmerge-n.md) per specificare la profondità dello spazio dei nomi supportata per la composizione di assembly di metadati. Ciò consente di configurare una suddivisione a caldo per i componenti Windows Runtime, in modo che solo un singolo file con estensione winmd sia in pacchetto anziché in molti. In questo modo si riducono i tempi di caricamento e l'I/O di file richiesti dalle app Windows Store.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti MIDLRT e Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




