---
title: Opzione /dlldata
description: L'opzione /dlldata viene usata per specificare il nome file per il file dlldata generato per una DLL proxy. Il nome file predefinito Dlldata.c viene usato se l'opzione /dlldata non è specificata.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- Opzione /dlldata MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1274226ae9768d45bb11e1a1f5b55caeddcc247a74a7ac08e03e3fcdacb0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105641"
---
# <a name="dlldata-switch"></a>Opzione /dlldata

**L'opzione /dlldata** viene usata per specificare il nome file per il file dlldata generato per una DLL proxy. Il nome file predefinito Dlldata.c viene usato se **l'opzione /dlldata** non è specificata.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*file-name* 
</dt> <dd>

Nome del file di origine C generato dal compilatore MIDL per la DLL proxy.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il file specificato da *file-name* deve essere collegato alla DLL proxy. Il file dlldata contiene i punti di ingresso e le strutture di dati richieste dal class factory per la DLL proxy. Queste strutture di dati specificano le interfacce oggetto contenute nella DLL proxy. Il file dlldata specifica anche l'identificatore di classe del class factory per la DLL proxy. Si tratta sempre dell'UUID (IID) della prima interfaccia del primo file proxy (in ordine alfabetico).

Lo stesso file dlldata deve essere specificato quando si richiama MIDL in tutti i file IDL che verranno in una determinata DLL proxy. Il file dlldata viene creato o aggiornato durante ogni compilazione MIDL, compilando in modo incrementale un elenco delle interfacce che andranno nella DLL proxy.

## <a name="examples"></a>Esempio

**midl /dlldata data.c**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




