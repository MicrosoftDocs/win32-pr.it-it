---
title: Salvataggio dell'output del preprocessore
description: La visualizzazione dell'output del preprocessore può essere un metodo efficace per la risoluzione dei problemi, ad esempio quando si verifica una sintassi del preprocessore IDL, C o C non valida o quando i valori -D fasulli nella riga di comando MIDL generano errori di tipo MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL del compilatore MIDL, salvataggio dell'output del preprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f016885ac4d669d7b62eaf3ff1d5ee3154f03d5eae64fca5f63c6111dff4c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641376"
---
# <a name="saving-preprocessor-output"></a>Salvataggio dell'output del preprocessore

La visualizzazione dell'output del preprocessore può essere un metodo efficace per la risoluzione dei problemi, ad esempio quando si verifica una sintassi del preprocessore IDL, C o C non valida o quando i valori -D fasulli nella riga di comando MIDL generano errori di tipo MIDL. Gli sviluppatori possono anche esaminare l'output del preprocessore per determinare quali file e definizioni erano presenti nel flusso di input del compilatore, ad esempio quando è necessario risolvere un caso difficile di conflitto di ridefinizione del tipo. O meno comunemente, alcuni sviluppatori potrebbero voler forzare i commutatori privati nel preprocessore con [**/cpp \_ opt**](-cpp-opt.md)o potrebbe voler vedere come funzionano le opzioni.

Il modo più semplice e meno invadente per ottenere i file pre-elaborati da un'esecuzione di compilazione MIDL è usare [**l'opzione -savePP.**](-savepp.md) **L'opzione -savePP** impedisce semplicemente a MIDL di eliminare i file temporanei passati dal preprocessore a MIDL. Considerare quanto segue:

**midl -savePP -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 -Oicf -env win32 stub.idl**

Questa direttiva compila Stub.idl, ma mantiene tutti i file del preprocessore.

> [!Note]  
> MIDL genera esecuzioni del preprocessore separate per i file IDL e ACF (se presenti) e per ogni file importato.

 

Per una compilazione DCOM, vengono in genere prodotti diversi file del preprocessore, anche se vengono elaborati da MIDL come flusso di input contiguo virtuale. In un ambiente Windows di programmazione, i file temporanei sono disponibili nella directory Temp come nomi di file, ad esempio MID \* .tmp. Se si conserva l'output del preprocessore, è consigliabile cercare i file recenti nella directory Temp per identificare i file associati a quale preprocessore viene eseguito.

In casi semplici, ad esempio quando il file IDL compilato non importa altri file direttamente o indirettamente o quando si esamina il file di primo livello, il preprocessore può essere richiamato direttamente. L'esecuzione diretta del preprocessore C/C++ può rivelare errori mascherati o confusi da MIDL. Ad esempio, le due righe di comando del preprocessore seguenti possono essere usate per la riga MIDL tra virgolette in precedenza:

**cl /E /nologo -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 stub.idl > stub.pp**

**cl /E /P -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 stub.idl**

Nel primo di questi due **esempi/E** [**/nologo**](-nologo.md) sono le opzioni aggiunte da MIDL quando si richiama il preprocessore. L'output del preprocessore viene inviato a stdout (schermata) e pertanto richiede il reindirizzamento a un file per l'esame. Nel secondo di questi esempi **/P** indica al preprocessore di reindirizzare l'output a un file I. In questo caso, nella directory corrente verrà creato un \* file Stub.i.

[**L'opzione /cpp \_ opt**](-cpp-opt.md) può essere usata anche per ottenere un file pre-elaborato, ma è difficile e inferiore ai metodi indicati in precedenza. L'esempio seguente produce anche un file Stub.i, come nell'esempio precedente. Le virgolette nell'esempio seguente sono essenziali:

**Midl -Oicf -win32 -cpp \_ opt "/E /P -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1" stub.idl**

 

 




