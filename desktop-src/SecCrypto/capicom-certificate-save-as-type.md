---
description: Definisce il formato di un file contenente le informazioni sul certificato.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Enumerazione CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328134"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="0b4b7-103">\_ \_ \_ Enumerazione di tipo Salva come certificato \_ CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0b4b7-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="0b4b7-104">Il tipo di enumerazione **\_ \_ Save \_ As \_ del certificato capicot** definisce il formato di un file contenente le informazioni sul certificato.</span><span class="sxs-lookup"><span data-stu-id="0b4b7-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="0b4b7-105">Questo tipo di enumerazione è stato introdotto da capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="0b4b7-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="0b4b7-106">Membri</span><span class="sxs-lookup"><span data-stu-id="0b4b7-106">Members</span></span>



| <span data-ttu-id="0b4b7-107">Membro</span><span class="sxs-lookup"><span data-stu-id="0b4b7-107">Member</span></span>                                  | <span data-ttu-id="0b4b7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b4b7-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="0b4b7-109">Valore</span><span class="sxs-lookup"><span data-stu-id="0b4b7-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0b4b7-110">**certificato capicol \_ \_ Salva \_ come \_ PFX**</span><span class="sxs-lookup"><span data-stu-id="0b4b7-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="0b4b7-111">Il file di output verrà formattato come file PFX (PKCS 12) e verranno salvate anche tutte le chiavi private associate esportabili.</span><span class="sxs-lookup"><span data-stu-id="0b4b7-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="0b4b7-112">0</span><span class="sxs-lookup"><span data-stu-id="0b4b7-112">0</span></span>     |
| <span data-ttu-id="0b4b7-113">**\_certificato CAPICOM \_ Salva \_ come \_ CER**</span><span class="sxs-lookup"><span data-stu-id="0b4b7-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="0b4b7-114">Il file di output verrà formattato come file con estensione CER senza chiavi private salvate.</span><span class="sxs-lookup"><span data-stu-id="0b4b7-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="0b4b7-115">1</span><span class="sxs-lookup"><span data-stu-id="0b4b7-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="0b4b7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b4b7-116">Remarks</span></span>

<span data-ttu-id="0b4b7-117">Il tipo di enumerazione del **certificato CApicol \_ \_ Salva \_ come \_** tipo viene usato dal metodo [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="0b4b7-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b4b7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b4b7-118">Requirements</span></span>



| <span data-ttu-id="0b4b7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b4b7-119">Requirement</span></span> | <span data-ttu-id="0b4b7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0b4b7-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4b7-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0b4b7-121">Redistributable</span></span><br/> | <span data-ttu-id="0b4b7-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b4b7-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0b4b7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b4b7-123">Header</span></span><br/>          | <dl> <span data-ttu-id="0b4b7-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b4b7-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




