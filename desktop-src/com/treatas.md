---
title: TreatAs
description: Specifica il CLSID di una classe in grado di emulare la classe corrente.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Chiave del registro di sistema Treats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856398"
---
# <a name="treatas"></a>TreatAs

Specifica il CLSID di una classe in grado di emulare la classe corrente.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** .

L'emulazione è la capacità di un'applicazione di aprire e modificare un oggetto di una classe diversa, mantenendo al tempo stesso il formato originale dell'oggetto. La risoluzione si verifica nel computer locale, quindi nel caso di attivazione remota la risoluzione si verifica nel computer client usando il CLSID specificato da **Treats**.

DCOM analizza il registro locale per i **trattati**, anche se si chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e si specifica un server remoto. Ciò significa che se si dispone di una voce **Treats** per Class1 da considerare come Class2 nel computer locale, ma si chiama **CoCreateInstance** per creare un'istanza di Class1 e si specifica un server remoto, DCOM tenterà di creare un'istanza di Class2 nel server remoto, anche se Class2 non è registrato nel server remoto, che causerà l'esito negativo della chiamata a **CoCreateInstance** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Autotreats**](autotreatas.md)
</dt> <dt>

[**CoGetTreatAsClass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




