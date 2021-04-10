---
title: Tre tipi di puntatore
description: MIDL supporta tre tipi di puntatori per supportare un'ampia gamma di applicazioni.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdcc9548568c8fca24d8abb40bf0eaa8b6e7da3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963126"
---
# <a name="three-pointer-types"></a>Tre tipi di puntatore

MIDL supporta tre tipi di puntatori per supportare un'ampia gamma di applicazioni. I tre livelli diversi sono detti puntatori di riferimento, univoco e completo e sono indicati rispettivamente dagli attributi **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**Unique**](/windows/desktop/Midl/unique) **\]** e **\[** [**ptr**](/windows/desktop/Midl/ptr) **\]** . Le classi del puntatore descritte da questi attributi si escludono a vicenda. È possibile applicare gli attributi del puntatore a puntatori in definizioni di tipo, tipi restituiti di funzioni, parametri di funzione, membri di strutture o unioni o elementi di matrice.

I puntatori incorporati sono i puntatori che sono membri di strutture o unioni. Possono anche essere elementi di matrici. Nella **\[** [](/windows/desktop/Midl/in) **\]** direzione, si presuppone che i puntatori **\[ ref \]** incorporati facciano riferimento a un archivio valido e non devono essere null. Questa situazione è applicabile in modo ricorsivo a tutti i puntatori **\[ ref \]** a cui puntano. Nella direzione **\[ , \]** i puntatori **\[ univoci \]** e completi incorporati (puntatori con l'attributo **\[ ptr \]** ) non possono essere null.

Qualsiasi attributo del puntatore posizionato su un parametro nella sintassi di una dichiarazione di funzione ha effetto solo sul dichiaratore di puntatore più a destra per il parametro. Per influenzare altri dichiaratori di puntatore, è necessario usare i tipi denominati intermedi.

Le funzioni che restituiscono un puntatore possono avere un attributo puntatore come attributo della funzione. È necessario applicare gli attributi **\[ Unique \]** e **\[ ptr \]** ai tipi restituiti della funzione. Le dichiarazioni di membro che sono puntatori possono specificare un attributo del puntatore come attributo di campo. Un attributo puntatore può essere applicato anche come attributo di tipo nei costrutti [**typedef**](/windows/desktop/Midl/typedef) .

Quando non è specificato alcun attributo puntatore come campo o attributo di tipo, gli attributi del puntatore vengono applicati in base alle regole per una dichiarazione di puntatore senza attributi, come indicato di seguito.

In modalità di compatibilità DCE, gli attributi del puntatore sono determinati nel file IDL di definizione. Se è presente un **\[** [**attributo \_ predefinito**](/windows/desktop/Midl/pointer-default) **\]** del puntatore specificato nell'interfaccia di definizione, viene usato tale attributo. Se non è presente alcun attributo **\[ \_ predefinito \] del puntatore** , tutti i puntatori senza attributi sono puntatori completi.

In modalità estensioni Microsoft, è possibile determinare gli attributi del puntatore importando i file IDL e applicati nell'ordine seguente:

1.  Attributo puntatore esplicito applicato al sito use.
2.  Attributo **\[ ref \]** , quando il puntatore senza attributi è un parametro del puntatore di primo livello.
3.  Attributo **\[ \_ predefinito \] del puntatore** specificato nell'interfaccia di definizione.
4.  Attributo **\[ \_ predefinito \] del puntatore** specificato nell'interfaccia di base.
5.  Attributo **\[ Unique \]** .

L' **\[** attributo dell'interfaccia [**\_ predefinita del puntatore**](/windows/desktop/Midl/pointer-default) **\]** specifica gli attributi del puntatore predefiniti da applicare a un dichiaratore di puntatore in un tipo, un parametro o una dichiarazione di tipo restituito quando alla dichiarazione non è applicato un attributo puntatore esplicito. L'attributo dell'interfaccia **\[ \_ predefinita \] del puntatore** non si applica a un puntatore di primo livello senza attributi di un parametro, che viene considerato **\[ ref \]**.

 

 