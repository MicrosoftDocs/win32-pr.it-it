---
title: Insertable (chiave CLSID)
description: Indica che gli oggetti di questa classe devono essere visualizzati nella casella di riepilogo della finestra di dialogo Inserisci oggetto quando vengono utilizzati dalle applicazioni contenitore COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Chiave del registro di sistema Insertable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047750"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="cf1f9-104">Insertable (chiave CLSID)</span><span class="sxs-lookup"><span data-stu-id="cf1f9-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="cf1f9-105">Indica che gli oggetti di questa classe devono essere visualizzati nella casella di riepilogo della finestra di dialogo **Inserisci oggetto** quando vengono utilizzati dalle applicazioni contenitore com.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="cf1f9-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="cf1f9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="cf1f9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf1f9-107">Remarks</span></span>

<span data-ttu-id="cf1f9-108">Questa chiave è una voce obbligatoria per le applicazioni COM a 32 bit i cui oggetti possono essere inseriti in applicazioni a 16 bit esistenti.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="cf1f9-109">Le applicazioni a 16 bit esistenti esaminano il registro di sistema per questa chiave, che informa l'applicazione che il server supporta l'incorporamento.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="cf1f9-110">Se la chiave **Insertable** esiste, le applicazioni a 16 bit possono anche tentare di verificare che il server esista nel computer.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="cf1f9-111">le applicazioni a 16 bit recuperano in genere il valore della chiave [**LocalServer**](localserver.md) dalla classe e verificano se è un file valido nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="cf1f9-112">Pertanto, per poter inserire un'applicazione a 32 bit da un'applicazione a 16 bit, è necessario che l'applicazione a 32 bit registri la sottochiave **LocalServer** oltre alla registrazione di [**LocalServer32**](localserver32.md).</span><span class="sxs-lookup"><span data-stu-id="cf1f9-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="cf1f9-113">Usato con i controlli, questa voce indica che un oggetto può fungere solo da oggetto incorporato sul posto senza funzionalità di controllo particolari.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="cf1f9-114">Gli oggetti che dispongono di questa chiave vengono visualizzati nella finestra di dialogo **Inserisci oggetto** per il relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="cf1f9-115">Quando viene usato con i controlli, questa voce indica anche che il controllo è stato testato con contenitori non di controllo.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="cf1f9-116">Anche questa voce è facoltativa e può essere omessa quando un controllo non è progettato per funzionare con i contenitori meno recenti che non sono in grado di riconoscere i controlli.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="cf1f9-117">Questa chiave non è presente per classi interne come le classi moniker.</span><span class="sxs-lookup"><span data-stu-id="cf1f9-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cf1f9-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf1f9-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




