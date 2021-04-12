---
title: Salvataggio dell'output del preprocessore
description: La visualizzazione dell'output del preprocessore può essere un metodo efficace per la risoluzione dei problemi, ad esempio quando si verifica una sintassi non valida per il preprocessore IDL, C o C, oppure quando i valori fittizi-D nella riga di comando MIDL generano errori arcani di segnalazione MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL Compiler MIDL, salvataggio dell'output del preprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396214"
---
# <a name="saving-preprocessor-output"></a>Salvataggio dell'output del preprocessore

La visualizzazione dell'output del preprocessore può essere un metodo efficace per la risoluzione dei problemi, ad esempio quando si verifica una sintassi non valida per il preprocessore IDL, C o C, oppure quando i valori fittizi-D nella riga di comando MIDL generano errori arcani di segnalazione MIDL. Gli sviluppatori possono anche esaminare l'output del preprocessore per determinare quali file e definizioni erano presenti nel flusso di input del compilatore, ad esempio quando è necessario risolvere un caso complesso di conflitti di ridefinizione dei tipi. O meno comunemente, determinati sviluppatori potrebbero voler forzare i commutatori privati sul preprocessore con [**/cpp \_ opt**](-cpp-opt.md)o vedere come funzionano i commutatori.

Il modo più semplice e meno intrusivo per ottenere i file pre-elaborati da un'esecuzione di compilazione MIDL consiste nell'usare l'opzione [**-savePP**](-savepp.md) . L'opzione **-savePP** impedisce semplicemente a MIDL di eliminare i file temporanei che il preprocessore passa di nuovo a MIDL. Considerare quanto segue:

**MIDL-savePP-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1-Oicf-ENV Win32 stub. idl**

Questa direttiva compila stub. idl, mantenendo tuttavia tutti i file del preprocessore.

> [!Note]  
> MIDL genera esecuzioni del preprocessore separate per il file IDL e ACF (se presente), nonché per ogni file importato.

 

Per una compilazione DCOM, in genere vengono prodotti diversi file del preprocessore, anche se vengono elaborati da MIDL come flusso di input contiguo virtuale. In un ambiente di programmazione Windows tipico, i file temporanei sono disponibili nella directory Temp come nomi di file, ad esempio MID \* . tmp. Se si conserva l'output del preprocessore, è consigliabile controllare i file recenti nella directory Temp per identificare quali file sono associati al preprocessore eseguito.

In casi semplici, ad esempio quando il file IDL compilato non importa altri file direttamente o indirettamente oppure quando si esamina il file di livello superiore, il preprocessore può essere richiamato direttamente. L'esecuzione diretta del preprocessore C/C++ può rivelare errori mascherati o confusi da MIDL. Ad esempio, le due righe di comando per il preprocessore seguenti possono essere utilizzate per la riga MIDL precedentemente racchiusa tra virgolette:

**CL/E/nologo-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. PP**

**CL/E/P-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl**

Nel primo di questi due esempi, **/e** [**/nologo**](-nologo.md) sono i commutatori aggiunti da MIDL quando si richiama il preprocessore. L'output del preprocessore viene inviato a stdout (schermata) e pertanto richiede il reindirizzamento a un file per l'analisi. Nel secondo di questi esempi, **/p** indica al preprocessore di reindirizzare l'output a un \* file con estensione i, in questo caso verrà creato un file stub. i nella directory corrente.

L'opzione [**/cpp \_ opt**](-cpp-opt.md) può essere usata anche per ottenere un file pre-elaborato, ma è difficile e inferiore ai metodi citati in precedenza. Nell'esempio seguente viene inoltre generato un file stub. i, come nell'esempio precedente. Le virgolette nell'esempio seguente sono essenziali:

**MIDL-Oicf-Win32-cpp \_ opz "/E/p-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1" Stub. idl**

 

 




