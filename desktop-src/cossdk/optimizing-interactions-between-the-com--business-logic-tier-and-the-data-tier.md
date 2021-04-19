---
description: Il livello dati contiene spesso principalmente informazioni statiche&\# 8212; le informazioni sono persistenti su supporti durevoli.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Ottimizzare le chiamate tra la logica di business e i dati COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304818"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="a2f0d-103">Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello dati</span><span class="sxs-lookup"><span data-stu-id="a2f0d-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="a2f0d-104">Il livello dati contiene spesso principalmente informazioni statiche, ovvero informazioni persistenti su supporti durevoli.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="a2f0d-105">Poiché questo livello comprende informazioni principalmente statiche, richiede un'analisi approfondita dei potenziali colli di bottiglia.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="a2f0d-106">Oltre alla possibilità ovvia di colli di bottiglia della connessione, le aree sensibili possono essere causate dai record a cui si accede di frequente, dai metodi di accesso ai dati non efficienti e dalla necessità di coordinare l'accesso ai sistemi legacy.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="a2f0d-107">Connessione al livello dati</span><span class="sxs-lookup"><span data-stu-id="a2f0d-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="a2f0d-108">Due considerazioni rivestono un ruolo importante nella progettazione di un livello dati per un'applicazione COM+: il pool di connessioni e l' [attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md)e l'utilizzo di DSN.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="a2f0d-109">I componenti che effettuano connessioni al livello dati devono utilizzare il [pool di oggetti com+](com--object-pooling.md) impostato sul componente.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="a2f0d-110">Quando si creano i DSN, utilizzare le stringhe del costruttore di oggetti specificate sul componente anziché creare un DSN di file.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="a2f0d-111">I DSN di file sono più lenti rispetto a una connessione utilizzando una stringa del costruttore di oggetti.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="a2f0d-112">È possibile specificare stringhe del costruttore di oggetti nella finestra delle proprietà del componente.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="a2f0d-113">Per altre informazioni, vedere [stringhe del costruttore di oggetti com+](com--object-constructor-strings.md).</span><span class="sxs-lookup"><span data-stu-id="a2f0d-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="a2f0d-114">Se si utilizzano componenti per accedere a un database di SQL Server, utilizzare il pool di oggetti COM+ anziché il pool di connessioni SQL.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="a2f0d-115">Se il componente usa ADO per recuperare più recordset, stabilire più connessioni per il componente.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="a2f0d-116">Quando ADO recupera più recordset, crea più connessioni in background se non vengono create.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="a2f0d-117">Se vengono create, è possibile raggrupparle e avere maggiore controllo sul numero di connessioni usate.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2f0d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2f0d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f0d-119">Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello di presentazione</span><span class="sxs-lookup"><span data-stu-id="a2f0d-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



