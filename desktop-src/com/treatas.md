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
# <a name="treatas"></a><span data-ttu-id="3846b-104">TreatAs</span><span class="sxs-lookup"><span data-stu-id="3846b-104">TreatAs</span></span>

<span data-ttu-id="3846b-105">Specifica il CLSID di una classe in grado di emulare la classe corrente.</span><span class="sxs-lookup"><span data-stu-id="3846b-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3846b-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3846b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="3846b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3846b-107">Remarks</span></span>

<span data-ttu-id="3846b-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="3846b-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="3846b-109">L'emulazione è la capacità di un'applicazione di aprire e modificare un oggetto di una classe diversa, mantenendo al tempo stesso il formato originale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3846b-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="3846b-110">La risoluzione si verifica nel computer locale, quindi nel caso di attivazione remota la risoluzione si verifica nel computer client usando il CLSID specificato da **Treats**.</span><span class="sxs-lookup"><span data-stu-id="3846b-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="3846b-111">DCOM analizza il registro locale per i **trattati**, anche se si chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e si specifica un server remoto.</span><span class="sxs-lookup"><span data-stu-id="3846b-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="3846b-112">Ciò significa che se si dispone di una voce **Treats** per Class1 da considerare come Class2 nel computer locale, ma si chiama **CoCreateInstance** per creare un'istanza di Class1 e si specifica un server remoto, DCOM tenterà di creare un'istanza di Class2 nel server remoto, anche se Class2 non è registrato nel server remoto, che causerà l'esito negativo della chiamata a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="3846b-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3846b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3846b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3846b-114">**Autotreats**</span><span class="sxs-lookup"><span data-stu-id="3846b-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="3846b-115">**CoGetTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="3846b-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="3846b-116">**CoTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="3846b-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




