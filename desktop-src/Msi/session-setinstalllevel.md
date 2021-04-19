---
description: Il metodo SetInstallLevel dell'oggetto Session imposta il livello di installazione per l'installazione corrente su un valore specificato e Ricalcola gli Stati Select e installato per tutte le funzionalità nella tabella Feature.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. SetInstallLevel, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333036"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="b24ab-103">Session. SetInstallLevel, metodo</span><span class="sxs-lookup"><span data-stu-id="b24ab-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="b24ab-104">Il metodo **SetInstallLevel** dell'oggetto [**Session**](session-object.md) imposta il livello di installazione per l'installazione corrente su un valore specificato e Ricalcola gli Stati Select e installato per tutte le funzionalità nella tabella Feature.</span><span class="sxs-lookup"><span data-stu-id="b24ab-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="b24ab-105">Imposta inoltre lo stato dell'azione di ogni componente nella [tabella dei componenti](component-table.md) in base al nuovo livello.</span><span class="sxs-lookup"><span data-stu-id="b24ab-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="b24ab-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b24ab-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="b24ab-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b24ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b24ab-108">*installLevel*</span><span class="sxs-lookup"><span data-stu-id="b24ab-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="b24ab-109">Richiesto nuovo livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="b24ab-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b24ab-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b24ab-110">Return value</span></span>

<span data-ttu-id="b24ab-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b24ab-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b24ab-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b24ab-112">Remarks</span></span>

<span data-ttu-id="b24ab-113">Prima di chiamare **SetInstallLevel** è necessario eseguire l' [azione CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b24ab-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="b24ab-114">Se viene passato 0 per il parametro *installLevel* , il livello di installazione corrente non viene modificato, ma tutte le funzionalità sono ancora aggiornate in base al livello di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="b24ab-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="b24ab-115">Questa funzionalità, ad esempio, può essere usata dal modulo handler per reimpostare tutte le selezioni sui rispettivi stati predefiniti iniziali in qualsiasi punto del processo di selezione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b24ab-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="b24ab-116">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="b24ab-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24ab-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b24ab-117">Requirements</span></span>



| <span data-ttu-id="b24ab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b24ab-118">Requirement</span></span> | <span data-ttu-id="b24ab-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b24ab-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b24ab-120">Versione</span><span class="sxs-lookup"><span data-stu-id="b24ab-120">Version</span></span><br/> | <span data-ttu-id="b24ab-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b24ab-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b24ab-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b24ab-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b24ab-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="b24ab-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b24ab-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b24ab-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="b24ab-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b24ab-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b24ab-126">IID</span><span class="sxs-lookup"><span data-stu-id="b24ab-126">IID</span></span><br/>     | <span data-ttu-id="b24ab-127">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b24ab-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




