---
title: Modifica degli attributi con l'interfaccia IDirectoryObject
description: Oltre a IADs put e IADs PutEx, è possibile usare il metodo IDirectoryObject SetObjectAttributes per modificare i valori degli attributi. Per usare questo metodo, è necessario compilare una struttura di \_ info attr Ads \_ per ogni attributo da modificare.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modifica degli attributi con l'interfaccia IDirectoryObject ADSI
- IDirectoryObject ADSI, utilizzo di per modificare gli attributi
- ADSI ADSI, esempio di codice C/C++, uso di IDirectoryObject per modificare gli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116680"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="4d85f-107">Modifica degli attributi con l'interfaccia IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="4d85f-107">Modifying Attributes with the IDirectoryObject Interface</span></span>

<span data-ttu-id="4d85f-108">Oltre a [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex), è possibile usare il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) per modificare i valori degli attributi.</span><span class="sxs-lookup"><span data-stu-id="4d85f-108">In addition to [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex), you can use the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method to modify attribute values.</span></span> <span data-ttu-id="4d85f-109">Per usare questo metodo, è necessario compilare una struttura [**di \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per ogni attributo da modificare.</span><span class="sxs-lookup"><span data-stu-id="4d85f-109">To use this method, you must fill in an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure for each attribute to modify.</span></span>

<span data-ttu-id="4d85f-110">Il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) consente di modificare gli attributi a valore singolo e multivalore.</span><span class="sxs-lookup"><span data-stu-id="4d85f-110">The [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method enables you to modify both single-valued and multi-valued attributes.</span></span> <span data-ttu-id="4d85f-111">Questa funzione fornisce controlli operativi simili, ad esempio Clear, Append, DELETE e Update, a quelli disponibili nel metodo [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="4d85f-111">This function provides similar operational controls, such as clear, append, delete, and update, to those found in the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span> <span data-ttu-id="4d85f-112">Le costanti di controllo includono:</span><span class="sxs-lookup"><span data-stu-id="4d85f-112">The control constants include:</span></span>

-   [<span data-ttu-id="4d85f-113">**Clear degli annunci \_ attr \_**</span><span class="sxs-lookup"><span data-stu-id="4d85f-113">**ADS\_ATTR\_CLEAR**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="4d85f-114">**\_aggiornamento attr \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="4d85f-114">**ADS\_ATTR\_UPDATE**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="4d85f-115">**\_accodamento degli annunci attr \_**</span><span class="sxs-lookup"><span data-stu-id="4d85f-115">**ADS\_ATTR\_APPEND**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="4d85f-116">**eliminazione degli annunci \_ attr \_**</span><span class="sxs-lookup"><span data-stu-id="4d85f-116">**ADS\_ATTR\_DELETE**</span></span>](adsi-attribute-modification-types.md)

<span data-ttu-id="4d85f-117">Se si specifica ADS, l' [**\_ \_ aggiornamento attr**](adsi-attribute-modification-types.md) attiverà un'operazione lato server che può richiedere un utilizzo intensivo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4d85f-117">Specifying [**ADS\_ATTR\_UPDATE**](adsi-attribute-modification-types.md) will trigger a server side operation that can be resource-intensive.</span></span> <span data-ttu-id="4d85f-118">Un esempio è costituito dall'avvio dell'operazione di aggiornamento di un lungo elenco di appartenenza al gruppo.</span><span class="sxs-lookup"><span data-stu-id="4d85f-118">An example would be to initiate the operation to update a long list of group membership.</span></span> <span data-ttu-id="4d85f-119">In generale, evitare di usare questa operazione, a meno che la modifica non includa un numero ridotto di attributi nella directory.</span><span class="sxs-lookup"><span data-stu-id="4d85f-119">In general, refrain from using this operation unless the modification involves a small number of attributes in the directory.</span></span> <span data-ttu-id="4d85f-120">Per modificare un lungo elenco di appartenenze a gruppi, l'approccio più efficiente consiste nel leggere l'elenco dalla directory sottostante, apportare modifiche e archiviare nuovamente l'elenco aggiornato nella directory.</span><span class="sxs-lookup"><span data-stu-id="4d85f-120">To modify a long list of group memberships, the more efficient approach would be to read the list from the underlying directory, make modifications, and store the updated list back to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="4d85f-121">Analogamente a [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) con [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), le modifiche degli attributi vengono completamente sottoposte a commit o scartate in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4d85f-121">Like [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) with [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), the attribute changes are either completely committed or discarded in Active Directory.</span></span> <span data-ttu-id="4d85f-122">Se una o più delle modifiche non sono consentite e pertanto non è possibile eseguirle, nessuna delle modifiche collettive apportate agli attributi viene sottoposta a commit nella directory.</span><span class="sxs-lookup"><span data-stu-id="4d85f-122">If one or more of the modifications are not allowed and therefore not able to be performed, then none of the collective modifications made to the attributes are committed to the directory.</span></span>

 

## <a name="example"></a><span data-ttu-id="4d85f-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="4d85f-123">Example</span></span>

<span data-ttu-id="4d85f-124">Nell'esempio di codice seguente viene illustrato come modificare gli attributi singoli e multivalore con il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="4d85f-124">The following code example shows how to modify both single and multi-valued attributes with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span>


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




