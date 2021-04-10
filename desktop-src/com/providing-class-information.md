---
title: Fornire informazioni sulla classe
description: Fornire informazioni sulla classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116816"
---
# <a name="providing-class-information"></a><span data-ttu-id="ea855-103">Fornire informazioni sulla classe</span><span class="sxs-lookup"><span data-stu-id="ea855-103">Providing Class Information</span></span>

<span data-ttu-id="ea855-104">Spesso è utile per un client di un oggetto esaminare le informazioni sul tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea855-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="ea855-105">Dato il CLSID dell'oggetto, un client può individuare la libreria dei tipi dell'oggetto utilizzando le voci del registro di sistema e quindi analizzare la libreria dei tipi per la voce della coclasse nella libreria che corrisponde al CLSID.</span><span class="sxs-lookup"><span data-stu-id="ea855-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="ea855-106">Tuttavia, non tutti gli oggetti hanno un CLSID, sebbene sia ancora necessario fornire informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="ea855-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="ea855-107">Inoltre, è utile per un client disporre di un modo per chiedere semplicemente a un oggetto le informazioni sul tipo, anziché passare attraverso la tedio per estrarre le stesse informazioni dalle voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ea855-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="ea855-108">Questa funzionalità è importante quando si gestiscono le interfacce in uscita sugli oggetti collegabili.</span><span class="sxs-lookup"><span data-stu-id="ea855-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="ea855-109">(Vedere [uso di IProvideClassInfo](using-iprovideclassinfo.md) per altre informazioni su come gli oggetti collegabili forniscono questa funzionalità).</span><span class="sxs-lookup"><span data-stu-id="ea855-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="ea855-110">In questi casi, un client può eseguire una query sull'oggetto per [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="ea855-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="ea855-111">Se queste interfacce esistono, il client chiama il metodo [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) per ottenere le informazioni sul tipo per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ea855-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="ea855-112">Implementando [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), un oggetto specifica che può fornire informazioni sul tipo per l'intera classe; ovvero ciò che verrebbe descritto nella relativa sezione di coclasse della relativa libreria dei tipi, se presente.</span><span class="sxs-lookup"><span data-stu-id="ea855-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="ea855-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) restituisce un puntatore **ITypeInfo** corrispondente alle informazioni sulla coclasse dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea855-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="ea855-114">Tramite questo puntatore **ITypeInfo** , il client può esaminare tutte le definizioni dell'interfaccia in entrata e in uscita dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea855-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="ea855-115">L'oggetto può anche fornire [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="ea855-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="ea855-116">L'interfaccia **IProvideClassInfo2** è una semplice estensione di [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) che consente di recuperare in modo semplice e rapido gli identificatori di interfaccia in uscita di un oggetto per il set di eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ea855-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="ea855-117">**IProvideClassInfo2** deriva da **IProvideClassInfo**.</span><span class="sxs-lookup"><span data-stu-id="ea855-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea855-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea855-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea855-119">Client e server COM</span><span class="sxs-lookup"><span data-stu-id="ea855-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




