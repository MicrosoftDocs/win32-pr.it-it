---
description: 'Controllo ortografico del testo del provider in modo più completo rispetto a ISpellCheckProvider:: check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Metodo IComprehensiveSpellCheckProvider:: ComprehensiveCheck'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319496"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="3da91-103">Metodo IComprehensiveSpellCheckProvider:: ComprehensiveCheck</span><span class="sxs-lookup"><span data-stu-id="3da91-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="3da91-104">Controllo ortografico del testo del provider in modo più completo rispetto a [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="3da91-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="3da91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3da91-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="3da91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3da91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da91-107">*testo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3da91-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da91-108">Testo da controllare.</span><span class="sxs-lookup"><span data-stu-id="3da91-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="3da91-109">*risultato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3da91-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da91-110">Risultato del controllo di questo testo, come enumerazione degli errori di ortografia ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), se presenti.</span><span class="sxs-lookup"><span data-stu-id="3da91-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da91-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3da91-111">Return value</span></span>

<span data-ttu-id="3da91-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3da91-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3da91-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3da91-113">Return value</span></span>                                                                             | <span data-ttu-id="3da91-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3da91-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3da91-115"><dt>\_OK</dt></span><span class="sxs-lookup"><span data-stu-id="3da91-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="3da91-116">Successo.</span><span class="sxs-lookup"><span data-stu-id="3da91-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="3da91-117"><dt>E \_ INVALIDARG</dt></span><span class="sxs-lookup"><span data-stu-id="3da91-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="3da91-118">il *testo* è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="3da91-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="3da91-119"><dt>\_puntatore E</dt></span><span class="sxs-lookup"><span data-stu-id="3da91-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="3da91-120">il *testo* è un puntatore null.</span><span class="sxs-lookup"><span data-stu-id="3da91-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="3da91-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3da91-121">Remarks</span></span>

<span data-ttu-id="3da91-122">Questa interfaccia non deve essere implementata da un provider di controllo ortografico.</span><span class="sxs-lookup"><span data-stu-id="3da91-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="3da91-123">Tuttavia, se il provider supporta due "modalità" di controllo ortografico (uno più veloce e più lento ma più completo), deve implementare questa interfaccia nello stesso oggetto che implementa [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) per supportare la modalità di controllo più approfondita.</span><span class="sxs-lookup"><span data-stu-id="3da91-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="3da91-124">Quando un client chiama [**ISpellChecker:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la funzionalità di controllo ortografico [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) il provider per [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)e chiama **IComprehensiveSpellCheckProvider. ComprehensiveCheck** se l'interfaccia è supportata.</span><span class="sxs-lookup"><span data-stu-id="3da91-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="3da91-125">Se l'interfaccia non è supportata, verrà eseguito automaticamente il fallback a [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="3da91-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="3da91-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3da91-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da91-127">**IComprehensiveSpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="3da91-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="3da91-128">**IEnumSpellingError**</span><span class="sxs-lookup"><span data-stu-id="3da91-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="3da91-129">**ISpellChecker:: ComprehensiveCheck**</span><span class="sxs-lookup"><span data-stu-id="3da91-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="3da91-130">**ISpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="3da91-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="3da91-131">**ISpellCheckProvider:: check**</span><span class="sxs-lookup"><span data-stu-id="3da91-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
