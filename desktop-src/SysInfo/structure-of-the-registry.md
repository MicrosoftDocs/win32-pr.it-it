---
description: Il Registro di sistema è un database gerarchico che contiene dati critici per il funzionamento di Windows e le applicazioni e i servizi eseguiti in Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struttura del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2eb63d49db37bc23eee56bb845c9c5dedf9df7ce4ce610ff8ade500e97cb88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763495"
---
# <a name="structure-of-the-registry"></a>Struttura del Registro di sistema

Il Registro di sistema è un database gerarchico che contiene dati critici per il funzionamento di Windows e le applicazioni e i servizi eseguiti in Windows. I dati sono strutturati in un formato albero. Ogni nodo nell'albero è denominato *chiave*. Ogni chiave può contenere *sia sottochiavi che* voci di dati denominate *valori*. In alcuni casi, la presenza di una chiave è di tutti i dati necessari per un'applicazione. altre volte, un'applicazione apre una chiave e usa i valori associati alla chiave. Una chiave può avere un numero qualsiasi di valori e i valori possono essere in qualsiasi formato. Per altre informazioni, vedere Tipi di valori [del Registro di sistema](registry-value-types.md) e Limiti delle dimensioni degli elementi del Registro di [sistema](registry-element-size-limits.md).

Ogni chiave ha un nome costituito da uno o più caratteri stampabili. Per i nomi delle chiavi non viene fatto distinzione tra maiuscole e minuscole. I nomi delle chiavi non possono includere il carattere barra rovesciata ( ), ma è possibile usare qualsiasi altro carattere \\ stampabile. I nomi e i dati dei valori possono includere il carattere barra rovesciata.

Il nome di ogni sottochiave è univoco rispetto alla chiave immediatamente superiore nella gerarchia. I nomi delle chiavi non sono localizzati in altre lingue, anche se i valori possono essere .

La figura seguente è una struttura di chiavi del Registro di sistema di esempio visualizzata dall'editor del Registro di sistema.

![Finestra dell'editor del Registro di sistema](images/regtree.png)

Ogni albero in **Computer locale** è una chiave. La **chiave HKEY \_ LOCAL \_ MACHINE** ha le sottochiavi **seguenti: HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** e **SYSTEM**. Ognuna di queste chiavi ha a sua volta sottochiavi. Ad esempio, la **chiave HARDWARE** include le sottochiavi **DESCRIPTION**, **DEVICEMAP** e **RESOURCEMAP**. la **chiave DEVICEMAP** ha diverse sottochiavi, tra cui **VIDEO**.

Ogni valore è costituito da un nome di valore e dai dati associati, se presenti. **MaxObjectNumber** e **VgaCompatible** sono valori che contengono dati nella **sottochiave VIDEO.**

Un albero del Registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del Registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del Registro Windows dati](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
