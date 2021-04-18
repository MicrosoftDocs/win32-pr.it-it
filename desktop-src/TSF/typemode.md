---
title: Enumerazione TYPEMODE (Softkbdc. h)
description: Gli elementi dell'enumerazione TYPEMODE vengono usati per specificare le modalità di tipo disponibili per una tastiera soft.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Framework servizi di testo enumerazione TYPEMODE
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301247"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="98629-104">Enumerazione TYPEMODE</span><span class="sxs-lookup"><span data-stu-id="98629-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="98629-105">Gli elementi dell'enumerazione **TYPEMODE** vengono usati per specificare le modalità di tipo disponibili per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="98629-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="98629-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98629-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="98629-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="98629-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="98629-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span><span class="sxs-lookup"><span data-stu-id="98629-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="98629-109">L'utente può fare clic sui tasti sullo schermo per digitare il testo.</span><span class="sxs-lookup"><span data-stu-id="98629-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="98629-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Passare il mouse**</span><span class="sxs-lookup"><span data-stu-id="98629-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="98629-111">L'utente può puntare a una chiave per un periodo di tempo predefinito e il carattere selezionato viene digitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="98629-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="98629-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Analisi**</span><span class="sxs-lookup"><span data-stu-id="98629-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="98629-113">La tastiera soft analizza continuamente l'area di input ed evidenzia le aree in cui l'utente può premere un tasto di scelta rapida o usare un dispositivo switch-input.</span><span class="sxs-lookup"><span data-stu-id="98629-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98629-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98629-114">Requirements</span></span>



| <span data-ttu-id="98629-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98629-115">Requirement</span></span> | <span data-ttu-id="98629-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98629-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98629-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98629-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98629-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98629-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98629-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98629-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98629-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98629-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="98629-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="98629-121">Redistributable</span></span><br/>          | <span data-ttu-id="98629-122">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98629-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="98629-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98629-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98629-124"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="98629-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="98629-125">IDL</span><span class="sxs-lookup"><span data-stu-id="98629-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98629-126"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98629-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





