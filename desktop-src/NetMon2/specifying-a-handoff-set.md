---
description: Un set di continuità specifica i protocolli che seguono un protocollo. Il parser utilizza un set di continuità solo quando il parser è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Specifica di un set di continuità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308157"
---
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="9756c-104">Specifica di un set di continuità</span><span class="sxs-lookup"><span data-stu-id="9756c-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="9756c-105">Un set di continuità specifica i protocolli che seguono un protocollo.</span><span class="sxs-lookup"><span data-stu-id="9756c-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="9756c-106">Il parser utilizza un set di continuità solo quando il parser è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="9756c-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="9756c-107">Il protocollo TCP, ad esempio, dispone di una proprietà Port che identifica il protocollo che segue il protocollo TCP.</span><span class="sxs-lookup"><span data-stu-id="9756c-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="9756c-108">Il valore della proprietà 20 indica che il protocollo successivo è FTP.</span><span class="sxs-lookup"><span data-stu-id="9756c-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="9756c-109">Il valore della proprietà 53 indica che il protocollo successivo è DNS.</span><span class="sxs-lookup"><span data-stu-id="9756c-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="9756c-110">Poiché la proprietà Port identifica il protocollo che segue, il parser TCP può usare il set di continuità seguente per ottenere un handle per il protocollo specificato dalla proprietà Port.</span><span class="sxs-lookup"><span data-stu-id="9756c-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

<span data-ttu-id="9756c-111">I set di continuità vengono archiviati nel file INI del parser.</span><span class="sxs-lookup"><span data-stu-id="9756c-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="9756c-112">Il set di continuità TCP precedente, ad esempio, si trova nel file tcpip.ini.</span><span class="sxs-lookup"><span data-stu-id="9756c-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="9756c-113">Si noti che se una DLL del parser supporta più protocolli, ogni parser che usa un set di continuità ha il proprio percorso nel file INI.</span><span class="sxs-lookup"><span data-stu-id="9756c-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="9756c-114">Le informazioni sui set di continuità vengono specificate durante l'implementazione della funzione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9756c-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="9756c-115">Il parser può specificare i protocolli che precedono il protocollo del parser e i protocolli che seguono il protocollo del parser.</span><span class="sxs-lookup"><span data-stu-id="9756c-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="9756c-116">Network Monitor accetta tutti i protocolli che precedono e aggiunge il protocollo del parser alle sezioni seguenti set del file INI del parser, per ogni protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="9756c-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="9756c-117">Network Monitor archivia l'elenco dei protocolli seguiti nella sezione set di continuità del file INI del parser.</span><span class="sxs-lookup"><span data-stu-id="9756c-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="9756c-118">Network Monitor archivia le informazioni sul set di continuità nel file INI del parser, ma il parser non accede direttamente ai file INI.</span><span class="sxs-lookup"><span data-stu-id="9756c-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="9756c-119">Per usare le informazioni nel set di continuità, il parser chiama la funzione [**CreateHandoffTable**](createhandofftable.md) per creare una tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="9756c-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="9756c-120">In genere, la tabella di continuità viene creata quando il parser registra il protocollo.</span><span class="sxs-lookup"><span data-stu-id="9756c-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="9756c-121">Dopo che il protocollo è stato registrato, Network Monitor crea una tabella set uniforme che può essere utilizzata dal parser.</span><span class="sxs-lookup"><span data-stu-id="9756c-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="9756c-122">Il parser usa il set di continuità quando riconoscono i dati.</span><span class="sxs-lookup"><span data-stu-id="9756c-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="9756c-123">Prima di tutto il parser legge il valore della proprietà che identifica il protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="9756c-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="9756c-124">Il parser chiama quindi [**GetProtocolFromTable**](getprotocolfromtable.md) per ottenere un handle per il protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="9756c-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="9756c-125">Infine, il parser restituisce un puntatore all'handle nel parametro *phNextProtocol* di [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="9756c-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 



