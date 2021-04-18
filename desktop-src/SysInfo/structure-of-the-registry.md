---
description: Il registro di sistema è un database gerarchico che contiene dati cruciali per il funzionamento di Windows e delle applicazioni e dei servizi eseguiti in Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struttura del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563424"
---
# <a name="structure-of-the-registry"></a>Struttura del registro di sistema

Il registro di sistema è un database gerarchico che contiene dati cruciali per il funzionamento di Windows e delle applicazioni e dei servizi eseguiti in Windows. I dati sono strutturati in un formato struttura ad albero. Ogni nodo dell'albero è denominato *chiave*. Ogni chiave può contenere sia *sottochiavi* che voci di dati denominate *valori*. In alcuni casi, la presenza di una chiave è costituita da tutti i dati richiesti da un'applicazione. in altri casi, un'applicazione apre una chiave e usa i valori associati alla chiave. Una chiave può avere un numero qualsiasi di valori e i valori possono essere in qualsiasi formato. Per altre informazioni, vedere [tipi di valore del registro](registry-value-types.md) di sistema e [limiti delle dimensioni degli elementi del registro](registry-element-size-limits.md).

Ogni chiave ha un nome costituito da uno o più caratteri stampabili. Per i nomi di chiave non viene fatta distinzione tra maiuscole I nomi di chiave non possono includere il carattere barra rovesciata ( \) , ma è possibile usare qualsiasi altro carattere stampabile. I nomi dei valori e i dati possono includere il carattere barra rovesciata.

Il nome di ogni sottochiave è univoco rispetto alla chiave immediatamente superiore nella gerarchia. I nomi delle chiavi non sono localizzati in altre lingue, anche se i valori possono essere.

Nella figura seguente è riportato un esempio di struttura di chiavi del registro di sistema come visualizzato dall'editor del registro di sistema.

![finestra dell'editor del registro di sistema](images/regtree.png)

Ogni albero sotto **computer locale** è una chiave. La chiave del **\_ \_ computer locale HKEY** presenta le sottochiavi seguenti: **hardware**, **Sam**, **Security**, **software** e **System**. Ognuna di queste chiavi a sua volta contiene sottochiavi. Ad esempio, la chiave **hardware** presenta le sottochiavi **Description**, **DEVICEMAP** e **RESOURCEMAP**; la chiave **DEVICEMAP** include diverse sottochiavi, incluso il **video**.

Ogni valore è costituito da un nome di valore e dai dati associati, se presenti. **MaxObjectNumber** e **VgaCompatible** sono valori che contengono dati nella sottochiave **video** .

Un albero del registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del registro di sistema di Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
