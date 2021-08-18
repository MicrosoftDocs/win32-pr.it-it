---
title: Tre tipi di puntatore
description: MIDL supporta tre tipi di puntatori per supportare un'ampia gamma di applicazioni.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9627c71b07c86ab2deb7e28bddcf6d30b1747cf7d44874620f4053383a5a948a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923460"
---
# <a name="three-pointer-types"></a>Tre tipi di puntatore

MIDL supporta tre tipi di puntatori per supportare un'ampia gamma di applicazioni. I tre livelli diversi sono denominati puntatori reference, unique e full e sono indicati rispettivamente dagli attributi **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**unique**](/windows/desktop/Midl/unique) **\]** e **\[** [**ptr.**](/windows/desktop/Midl/ptr) **\]** Le classi puntatore descritte da questi attributi si escludono a vicenda. Gli attributi del puntatore possono essere applicati ai puntatori in definizioni di tipo, tipi restituiti di funzioni, parametri di funzione, membri di strutture o unioni o elementi di matrice.

I puntatori incorporati sono puntatori membri di strutture o unioni. Possono anche essere elementi di matrici. Nella direzione **\[** [**,**](/windows/desktop/Midl/in) **\]** si presuppone che i puntatori **\[ di \]** riferimento incorporati puntino a una risorsa di archiviazione valida e non devono essere Null. Questa situazione è applicabile in modo ricorsivo a tutti i puntatori **\[ di \]** riferimento a cui puntano. Nella direzione **\[ in \]** , i **\[ puntatori univoci \]** e completi incorporati (puntatori con l'attributo **\[ ptr) \]** possono o meno essere Null.

Qualsiasi attributo puntatore posizionato su un parametro nella sintassi di una dichiarazione di funzione influisce solo sul dichiaratore di puntatore più a destra per tale parametro. Per influire su altri dichiaratori di puntatore, è necessario usare tipi denominati intermedi.

Le funzioni che restituiscono un puntatore possono avere un attributo puntatore come attributo di funzione. Gli **\[ attributi unique \]** e **\[ ptr \]** devono essere applicati ai tipi restituiti della funzione. Le dichiarazioni di membro che sono puntatori possono specificare un attributo puntatore come attributo di campo. Un attributo puntatore può essere applicato anche come attributo di tipo nei [**costrutti typedef.**](/windows/desktop/Midl/typedef)

Quando non viene specificato alcun attributo puntatore come attributo di campo o tipo, gli attributi del puntatore vengono applicati in base alle regole per una dichiarazione di puntatore senza attributi, come indicato di seguito.

In modalità di compatibilità DCE, gli attributi del puntatore vengono determinati nel file IDL di definizione. Se nell'interfaccia di definizione è specificato un attributo predefinito del puntatore, viene usato tale **\[** [**\_**](/windows/desktop/Midl/pointer-default) **\]** attributo. Se non **\[ è presente alcun \_ attributo \]** predefinito del puntatore, tutti i puntatori senza attributi sono puntatori completi.

In modalità estensioni Microsoft, gli attributi del puntatore possono essere determinati importando file IDL e vengono applicati nell'ordine seguente:

1.  Attributo puntatore esplicito applicato nel sito di utilizzo.
2.  Attributo **\[ ref, \]** quando il puntatore senza attributi è un parametro puntatore di primo livello.
3.  Attributo **\[ predefinito del \_ puntatore \]** specificato nell'interfaccia di definizione.
4.  Attributo **\[ predefinito del \_ puntatore \]** specificato nell'interfaccia di base.
5.  Attributo **\[ \] univoco.**

L'attributo dell'interfaccia predefinita del puntatore specifica gli attributi del puntatore predefiniti da applicare a un dichiaratore di puntatore in una dichiarazione di tipo, parametro o tipo restituito quando a tale dichiarazione non è applicato un attributo puntatore **\[** [**\_**](/windows/desktop/Midl/pointer-default) **\]** esplicito. **\[ \_ L'attributo \] dell'interfaccia** predefinita del puntatore non si applica a un puntatore di primo livello senza attributi di un parametro, che si presuppone sia **\[ ref \]**.

 

 