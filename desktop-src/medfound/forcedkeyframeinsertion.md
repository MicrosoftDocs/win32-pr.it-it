---
description: Inserimento fotogramma chiave forzata
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserimento fotogramma chiave forzata (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484076"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="54ebc-103">Inserimento fotogramma chiave forzata (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="54ebc-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="54ebc-104">Quando si configura un oggetto codificatore video, è possibile impostare un intervallo massimo per i fotogrammi chiave nel contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="54ebc-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="54ebc-105">Tuttavia, il codec inserisce i fotogrammi chiave nell'intervallo indicato dal contenuto; l'intervallo del fotogramma chiave non è costante.</span><span class="sxs-lookup"><span data-stu-id="54ebc-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="54ebc-106">Per alcune applicazioni, la distanza del fotogramma chiave è molto importante.</span><span class="sxs-lookup"><span data-stu-id="54ebc-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="54ebc-107">Ad esempio, un'applicazione di modifica video necessita di fotogrammi chiave nei percorsi logici di un editor, ad esempio le interruzioni di scena e le transizioni di tipo Shot.</span><span class="sxs-lookup"><span data-stu-id="54ebc-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="54ebc-108">L'inserimento di fotogrammi chiave forzata è una funzionalità che consente di richiedere la codifica di un frame di input come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="54ebc-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="54ebc-109">Il codificatore tenterà di rispettare queste richieste, ma le impostazioni del buffer (velocità in bit e finestra del buffer) configurate per la sessione di codifica hanno sempre la precedenza.</span><span class="sxs-lookup"><span data-stu-id="54ebc-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="54ebc-110">Gli oggetti del codificatore video implementano l'inserimento di fotogrammi chiave forzata come risposta a un'estensione dell'unità dati associata all'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="54ebc-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="54ebc-111">Per ulteriori informazioni sulle estensioni dell'unità dati, vedere [Using Data Unit Extensions](usingdataunitextensions.md).</span><span class="sxs-lookup"><span data-stu-id="54ebc-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="54ebc-112">I dati dell'estensione per l'inserimento di fotogrammi chiave forzata sono identificati dal valore GUID seguente: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span><span class="sxs-lookup"><span data-stu-id="54ebc-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="54ebc-113">Le singole estensioni sono valori **bool** .</span><span class="sxs-lookup"><span data-stu-id="54ebc-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="54ebc-114">Impostare il valore su **true** per indicare una richiesta del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="54ebc-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54ebc-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54ebc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ebc-116">Uso delle estensioni dell'unità dati</span><span class="sxs-lookup"><span data-stu-id="54ebc-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="54ebc-117">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="54ebc-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



