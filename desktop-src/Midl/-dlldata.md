---
title: opzione/dlldata
description: L'opzione/dlldata viene usata per specificare il nome file per il file dlldata generato per una DLL proxy. Se non si specifica l'opzione/dlldata, viene usato il nome file predefinito dlldata. c.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata switch MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718691"
---
# <a name="dlldata-switch"></a>opzione/dlldata

L'opzione **/dlldata** viene usata per specificare il nome file per il file dlldata generato per una DLL proxy. Se non si specifica l'opzione **/dlldata** , viene usato il nome file predefinito dlldata. c.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*nome file* 
</dt> <dd>

Nome del file di origine C che il compilatore MIDL genererà per la DLL del proxy.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il file specificato da *nome file* deve essere collegato alla DLL del proxy. Il file dlldata contiene i punti di ingresso e le strutture di dati richiesti dall'class factory per la DLL del proxy. Queste strutture di dati specificano le interfacce oggetto contenute nella DLL del proxy. Il file dlldata specifica anche l'identificatore di classe del class factory per la DLL del proxy. Si tratta sempre dell'UUID (IID) della prima interfaccia del primo file proxy (in ordine alfabetico).

È necessario specificare lo stesso file dlldata quando si richiama MIDL in tutti i file IDL che entreranno in una determinata DLL del proxy. Il file dlldata viene creato o aggiornato durante ogni compilazione MIDL, compilando in modo incrementale un elenco delle interfacce che verranno inserite nella DLL del proxy.

## <a name="examples"></a>Esempio

**MIDL/dlldata data. c**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




