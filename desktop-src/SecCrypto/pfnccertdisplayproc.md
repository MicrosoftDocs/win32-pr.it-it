---
description: Funzione di callback definita dall'utente che consente al chiamante della funzione CryptUIDlgSelectCertificate di gestire la visualizzazione dei certificati selezionati dall'utente per la visualizzazione.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Funzione di callback PFNCCERTDISPLAYPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050075"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="1337b-103">Funzione di callback PFNCCERTDISPLAYPROC</span><span class="sxs-lookup"><span data-stu-id="1337b-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="1337b-104">La funzione **PFNCCERTDISPLAYPROC** è una funzione di callback definita dall'utente che consente al chiamante della funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) di gestire la visualizzazione dei certificati selezionati dall'utente per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1337b-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="1337b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1337b-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="1337b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1337b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1337b-107">*pCertContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1337b-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1337b-108">Puntatore a una struttura [**del \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato che rappresenta il certificato da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="1337b-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="1337b-109">*hWndSelCertDlg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1337b-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1337b-110">Handle per la finestra di dialogo da cui è stato selezionato il certificato per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1337b-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="1337b-111">*pvCallbackData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1337b-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1337b-112">Dati aggiuntivi utilizzati dalla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="1337b-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1337b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1337b-113">Return value</span></span>

<span data-ttu-id="1337b-114">Questa funzione restituisce **true** per indicare che gestisce la visualizzazione del certificato e che la finestra di dialogo non deve visualizzare il certificato.</span><span class="sxs-lookup"><span data-stu-id="1337b-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="1337b-115">Se questa funzione restituisce **false**, nella finestra di dialogo verrà visualizzato il certificato.</span><span class="sxs-lookup"><span data-stu-id="1337b-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="1337b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1337b-116">Requirements</span></span>



| <span data-ttu-id="1337b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1337b-117">Requirement</span></span> | <span data-ttu-id="1337b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1337b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1337b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1337b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1337b-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1337b-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1337b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1337b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1337b-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1337b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




