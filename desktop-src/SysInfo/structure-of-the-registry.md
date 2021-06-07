---
description: Il Registro di sistema è un database gerarchico che contiene dati fondamentali per il funzionamento di Windows e per le applicazioni e i servizi eseguiti in Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struttura del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386670"
---
# <a name="structure-of-the-registry"></a>Struttura del Registro di sistema

Il Registro di sistema è un database gerarchico che contiene dati fondamentali per il funzionamento di Windows e per le applicazioni e i servizi eseguiti in Windows. I dati sono strutturati in un formato albero. Ogni nodo nell'albero è denominato *chiave*. Ogni chiave può contenere *sia sottochiavi* che voci di dati denominate *valori*. In alcuni casi, la presenza di una chiave è di tutti i dati necessari per un'applicazione. in altri casi, un'applicazione apre una chiave e usa i valori associati alla chiave. Una chiave può avere un numero qualsiasi di valori e i valori possono essere in qualsiasi forma. Per altre informazioni, vedere [Tipi di valori del Registro di sistema e](registry-value-types.md) Limiti delle dimensioni degli elementi del Registro di [sistema.](registry-element-size-limits.md)

Ogni chiave ha un nome costituito da uno o più caratteri stampabili. I nomi delle chiavi non supportano la distinzione tra maiuscole e minuscole. I nomi delle chiavi non possono includere il carattere barra rovesciata ( ), ma è possibile usare qualsiasi altro carattere \\ stampabile. I nomi e i dati dei valori possono includere il carattere barra rovesciata.

Il nome di ogni sottochiave è univoco rispetto alla chiave immediatamente superiore nella gerarchia. I nomi delle chiavi non sono localizzati in altre lingue, anche se i valori possono essere .

Nella figura seguente è riportata una struttura di chiavi del Registro di sistema di esempio visualizzata dall'editor del Registro di sistema.

![finestra dell'editor del Registro di sistema](images/regtree.png)

Ogni albero in **Computer locale** è una chiave. La **chiave HKEY \_ LOCAL \_ MACHINE** ha le sottochiavi **seguenti: HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** e **SYSTEM.** Ognuna di queste chiavi a sua volta ha sottochiavi. Ad esempio, la **chiave HARDWARE** contiene le sottochiavi **DESCRIPTION**, **DEVICEMAP** e **RESOURCEMAP**; La **chiave DEVICEMAP** ha diverse sottochiavi, tra cui **VIDEO**.

Ogni valore è costituito da un nome di valore e dai dati associati, se presenti. **MaxObjectNumber** e **VgaCompatible** sono valori che contengono dati nella **sottochiave VIDEO.**

Un albero del Registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del Registro di sistema di Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
