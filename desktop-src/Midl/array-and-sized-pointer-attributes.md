---
title: Attributi array e Sized-Pointer
description: MIDL offre un set completo di funzionalità per il passaggio di matrici di dati e puntatori ai dati. È possibile utilizzare questi attributi per specificare le caratteristiche di matrici e più livelli di puntatori.
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- MIDL, attributi, matrici e puntatore a dimensione di IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872418"
---
# <a name="array-and-sized-pointer-attributes"></a>Attributi array e Sized-Pointer

MIDL offre un set completo di funzionalità per il passaggio di matrici di dati e puntatori ai dati. È possibile utilizzare questi attributi per specificare le caratteristiche di matrici e più livelli di puntatori.



| Attributo                       | Utilizzo                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dimensioni \_**](size-is.md)     | Specifica la quantità di memoria da allocare per i puntatori dimensionati, i puntatori dimensionati ai puntatori di dimensione e le matrici mono o multidimensionali.                                                         |
| [**Max \_ è**](max-is.md)       | Valore massimo per un indice di matrice.                                                                                                                                                                |
| [**lunghezza \_**](length-is.md) | Numero di elementi della matrice da trasmettere.                                                                                                                                                      |
| [**il primo \_ è**](first-is.md)   | Indice del primo elemento di matrice da trasmettere.                                                                                                                                              |
| [**ultimo \_ è**](last-is.md)     | Fornisce l'indice dell'ultimo elemento della matrice da trasmettere.                                                                                                                                         |
| [**string**](string.md)        | Indica che la matrice unidimensionale [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) o il puntatore a tale matrice deve essere gestita come stringa. |
| [**intervallo**](range.md)          | Specifica un intervallo di valori consentiti per argomenti o campi i cui valori sono impostati in fase di esecuzione.                                                                                                       |



 

MIDL supporta tre tipi di puntatori: puntatori di riferimento, puntatori univoci e puntatori completi. Questi puntatori sono specificati dagli attributi [**ref**](ref.md), [**Unique**](unique.md)e [**ptr**](ptr.md)del puntatore.

Un attributo del puntatore può essere applicato come attributo di tipo; come attributo di campo che si applica a un membro di struttura, a un membro di Unione o a un parametro; o come attributo di funzione applicabile al tipo restituito della funzione. L'attributo pointer può essere visualizzato anche con la parola chiave [**\_ default del puntatore**](pointer-default.md) .

Per consentire a un parametro del puntatore di cambiare valore durante una funzione remota, è necessario fornire un altro livello di riferimento indiretto fornendo più dichiaratori di puntatore. L'attributo puntatore esplicito applicato al parametro ha effetto solo sul dichiaratore di puntatore più a destra per il parametro. Quando sono presenti più dichiaratori di puntatore in una dichiarazione di parametro, gli altri dichiaratori vengono predefiniti per l'attributo del puntatore specificato dall'attributo [**\_ predefinito del puntatore**](pointer-default.md) . Per applicare attributi puntatore diversi a più dichiaratori di puntatore, è necessario definire tipi intermedi che specificano gli attributi del puntatore esplicito.

## <a name="default-pointer-attribute-values"></a>Valori Pointer-Attribute predefiniti

Quando nessun attributo puntatore è associato a un puntatore che è un parametro, il puntatore viene considerato un puntatore [**ref**](ref.md) .

Quando nessun attributo puntatore è associato a un puntatore che è membro di una struttura o di un'Unione, il compilatore MIDL assegna gli attributi del puntatore usando le seguenti regole di priorità (1 è più alto):

1.  Attributi applicati in modo esplicito al tipo di puntatore
2.  Attributi applicati in modo esplicito al parametro o al membro del puntatore
3.  Attributo [**\_ predefinito del puntatore**](pointer-default.md) nel file IDL che definisce il tipo
4.  Attributo [**\_ predefinito del puntatore**](pointer-default.md) nel file IDL che importa il tipo
5.  [**ptr**](ptr.md) (modalità OSF); [**Unique**](unique.md) (modalità predefinita di Microsoft RPC)

Quando il file IDL viene compilato in modalità predefinita, i file importati possono ereditare gli attributi del puntatore dall'importazione di file. Questa funzionalità non è disponibile quando si esegue la compilazione con l'opzione/[**OSF**](-osf.md) . Per ulteriori informazioni, vedere [**Import**](import.md).

## <a name="function-return-types"></a>Tipi restituiti dalla funzione

Un puntatore restituito da una funzione deve essere un puntatore [**univoco**](unique.md) o un puntatore completo. Il compilatore MIDL segnala un errore se il risultato di una funzione è un puntatore di riferimento, in modo esplicito o per impostazione predefinita. Il puntatore restituito indica sempre la nuova risorsa di archiviazione.

Le funzioni che restituiscono un valore di puntatore possono specificare un attributo del puntatore come attributo della funzione. Se non è presente un attributo puntatore, il puntatore del risultato della funzione utilizzerà il valore fornito come attributo [**\_ predefinito del puntatore**](pointer-default.md) .

## <a name="pointer-attributes-in-type-definitions"></a>Attributi puntatore nelle definizioni di tipo

Quando si specifica un attributo puntatore al livello principale di un'istruzione [**typedef**](typedef.md) , l'attributo specificato viene applicato al dichiaratore puntatore, come previsto. Quando non viene specificato alcun attributo puntatore, i dichiaratori di puntatore al livello superiore di un'istruzione typedef ereditano il tipo di attributo del puntatore quando vengono utilizzati.

DCE IDL non consente di applicare esplicitamente lo stesso attributo puntatore due volte, ad esempio nella Dichiarazione [**typedef**](typedef.md) e nell'elenco di attributi dei parametri. Quando si usa la modalità predefinita (Microsoft Extensions) del compilatore MIDL, questo vincolo è rilassato.

Per informazioni sull'uso di matrici e puntatori MIDL in chiamate a procedure remote, vedere [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).

 

 