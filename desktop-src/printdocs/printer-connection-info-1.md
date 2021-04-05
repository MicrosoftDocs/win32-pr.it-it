---
description: Rappresenta le informazioni su una connessione a una stampante.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Struttura PRINTER_CONNECTION_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757382"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="7f4b7-103">Struttura delle informazioni di connessione della stampante \_ \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="7f4b7-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="7f4b7-104">Rappresenta le informazioni su una connessione a una stampante.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f4b7-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="7f4b7-106">Members</span><span class="sxs-lookup"><span data-stu-id="7f4b7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f4b7-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="7f4b7-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7f4b7-108">Vengono definiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f4b7-108">The following values are defined:</span></span>



| <span data-ttu-id="7f4b7-109">Valore</span><span class="sxs-lookup"><span data-stu-id="7f4b7-109">Value</span></span>                                      | <span data-ttu-id="7f4b7-110">Significato</span><span class="sxs-lookup"><span data-stu-id="7f4b7-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4b7-111">\_ \_ Mancata corrispondenza della connessione stampante (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="7f4b7-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="7f4b7-112">Se questo flag di bit è impostato, la connessione alla stampante non corrisponde.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="7f4b7-113">L'utente può fornire un driver di stampa locale come *pszDriverName* e utilizzarlo per eseguire il rendering anziché utilizzare il driver installato nella stampante server a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="7f4b7-114">\_Connessione stampante \_ senza \_ interfaccia utente (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="7f4b7-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="7f4b7-115">Se viene impostato questo flag di bit, questa chiamata non potrà visualizzare una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="7f4b7-116">Se è necessario visualizzare una finestra di dialogo per installare un driver della stampante dal server e questo flag di bit è impostato, il driver della stampante non verrà installato, la connessione alla stampante non verrà aggiunta e la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="7f4b7-117">**Windows 7:** In Windows 7 e nelle versioni successive di Windows, se questo flag è impostato e l'utente è in esecuzione in modalità con privilegi elevati, la finestra di dialogo **attendibile per la stampante?** non verrà visualizzata.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f4b7-118">**pszDriverName**</span><span class="sxs-lookup"><span data-stu-id="7f4b7-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="7f4b7-119">Puntatore al nome del driver.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f4b7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f4b7-120">Requirements</span></span>



| <span data-ttu-id="7f4b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4b7-121">Requirement</span></span> | <span data-ttu-id="7f4b7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7f4b7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4b7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f4b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4b7-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f4b7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7f4b7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f4b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4b7-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f4b7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7f4b7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f4b7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4b7-128"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f4b7-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4b7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f4b7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4b7-130">Stampa</span><span class="sxs-lookup"><span data-stu-id="7f4b7-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7f4b7-131">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="7f4b7-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




