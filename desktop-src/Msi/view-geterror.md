---
description: Il metodo getError dell'oggetto View restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View. GetError, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326535"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="dec5b-103">View. GetError, metodo</span><span class="sxs-lookup"><span data-stu-id="dec5b-103">View.GetError method</span></span>

<span data-ttu-id="dec5b-104">Il metodo **GetError** dell'oggetto [**View**](view-object.md) restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="dec5b-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="dec5b-105">In automazione, il valore restituito è una stringa nel formato \# \# ColumnName, dove \# \# rappresenta un codice di errore a 2 cifre.</span><span class="sxs-lookup"><span data-stu-id="dec5b-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="dec5b-106">Restituisce il primo errore nella matrice di errori della visualizzazione. le chiamate successive restituiscono il valore successivo nella matrice di errori.</span><span class="sxs-lookup"><span data-stu-id="dec5b-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="dec5b-107">Quando viene restituito il valore '00 ', non sono presenti altri errori e le chiamate successive passano di nuovo a scorrere la matrice.</span><span class="sxs-lookup"><span data-stu-id="dec5b-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec5b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dec5b-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="dec5b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dec5b-109">Parameters</span></span>

<span data-ttu-id="dec5b-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dec5b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dec5b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dec5b-111">Return value</span></span>

<span data-ttu-id="dec5b-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dec5b-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec5b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dec5b-113">Requirements</span></span>



| <span data-ttu-id="dec5b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec5b-114">Requirement</span></span> | <span data-ttu-id="dec5b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dec5b-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec5b-116">Versione</span><span class="sxs-lookup"><span data-stu-id="dec5b-116">Version</span></span><br/> | <span data-ttu-id="dec5b-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dec5b-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dec5b-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dec5b-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dec5b-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="dec5b-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dec5b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dec5b-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="dec5b-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec5b-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dec5b-122">IID</span><span class="sxs-lookup"><span data-stu-id="dec5b-122">IID</span></span><br/>     | <span data-ttu-id="dec5b-123">IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dec5b-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




