---
description: 'I modelli definiscono la modalità di interpretazione del flusso di dati: i dati vengono modulati dalla definizione del modello. In questa sezione vengono illustrati gli aspetti seguenti di un modello e viene fornito un modello di esempio.'
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modelli (formato di file X, codifica del testo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e164b92c6c5738ad98b138941b1b2fda6c332068
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881024"
---
# <a name="templates-x-file-format-text-encoding"></a>Modelli (formato di file X, codifica del testo)

I modelli definiscono la modalità di interpretazione del flusso di dati: i dati vengono modulati dalla definizione del modello. In questa sezione vengono illustrati gli aspetti seguenti di un modello e viene fornito un modello di esempio.

Esiste un modello speciale, il modello di intestazione. È consigliabile che ogni applicazione defini un modello di intestazione e lo usi per definire informazioni specifiche dell'applicazione, ad esempio le informazioni sulla versione. Se presente, questa intestazione viene letta dall'API di formato di file con estensione x. Se è disponibile un membro flags, viene usato per determinare come vengono interpretati i dati seguenti. Il membro flags, se definito, deve essere un valore DWORD. Un bit è attualmente definito, il bit 0. Se questo bit è chiaro, i dati seguenti nel file sono binari. Se impostato, i dati seguenti sono testo. È possibile usare più oggetti dati di intestazione per passare dal testo binario al testo all'interno del file.

## <a name="template-form-name-and-uuid"></a>Modulo modello, nome e UUID

Un modello ha il formato seguente.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



Il nome del modello è un nome alfanumerico che può includere il carattere di sottolineatura ( \_ ). Non deve iniziare con una cifra. L'UUID è un identificatore univoco universalmente formattato con lo standard Distributed Computing Environment di Open Software Foundation e racchiuso tra parentesi angolari (< >). Ad esempio: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.

## <a name="template-members"></a>Membri del modello

I membri del modello sono costituiti da un tipo di dati denominato seguito da un nome facoltativo o da una matrice di un tipo di dati denominato. Nella tabella seguente sono definiti tipi di dati primitivi validi.



| Tipo    | Dimensione                               |
|---------|------------------------------------|
| WORD    | 16 bit                            |
| DWORD   | 32 bit                            |
| FLOAT   | Float IEEE                         |
| DOUBLE  | 64 bit                            |
| CHAR    | 8 bit                             |
| UCHAR   | 8 bit                             |
| BYTE    | 8 bit                             |
| STRING  | Stringa con terminazione NULL             |
| CSTRING | Stringa C formattata (non supportata) |
| UNICODE | Stringa Unicode (non supportata)     |



 

È anche possibile fare riferimento a tipi di dati aggiuntivi definiti dai modelli rilevati in precedenza nel flusso di dati all'interno di una definizione di modello. Non sono consentiti riferimenti in avanti.

Qualsiasi tipo di dati valido può essere espresso come matrice nella definizione del modello. La sintassi di base è illustrata nell'esempio seguente.


```
array <data-type> <name>[<dimension-size>];
```



&lt;dimension-size può essere un numero intero o un riferimento denominato a un altro membro &gt; modello il cui valore viene quindi sostituito. Le matrici possono essere n-dimensionali, dove n è determinato dal numero di parentesi quadre abbinate che hanno come fine l'istruzione , come nell'esempio seguente.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Restrizioni dei modelli

I modelli possono essere aperti, chiusi o limitati. Queste restrizioni determinano quali tipi di dati possono essere visualizzati nella gerarchia immediata di un oggetto dati definito dal modello. Un modello aperto non presenta restrizioni, un modello chiuso rifiuta tutti i tipi di dati e un modello con restrizioni consente un elenco denominato di tipi di dati.

La sintassi per indicare un modello aperto è di tre punti racchiusi tra parentesi quadre.


```
[ ... ]
```



Un elenco delimitato da virgole di tipi di dati denominati seguito facoltativamente dai relativi UUID racchiusi tra parentesi quadre indica un modello con restrizioni.


```
[ { data-type [ UUID ] , } ... ]
```



L'assenza di uno dei precedenti indica un modello chiuso.

## <a name="template-example"></a>Esempio di modello

Di seguito viene illustrato un modello di esempio.


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica testo](text-encoding.md)
</dt> </dl>

 

 



