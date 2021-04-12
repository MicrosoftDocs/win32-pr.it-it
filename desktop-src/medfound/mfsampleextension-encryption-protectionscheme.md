---
description: Specifica lo schema di protezione per gli esempi crittografati.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: Attributo MFSampleExtension_Encryption_ProtectionScheme (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131122"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="2b4bc-103">\_Attributo ProtectionScheme di crittografia MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="2b4bc-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="2b4bc-104">Specifica lo schema di protezione per gli esempi crittografati.</span><span class="sxs-lookup"><span data-stu-id="2b4bc-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b4bc-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2b4bc-105">Data type</span></span>

<span data-ttu-id="2b4bc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2b4bc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2b4bc-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b4bc-107">Remarks</span></span>

<span data-ttu-id="2b4bc-108">Il valore di questo attributo è un membro dell'enumerazione [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) .</span><span class="sxs-lookup"><span data-stu-id="2b4bc-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="2b4bc-109">Nei casi in cui l'origine multimediale è basata su MP4, il valore viene impostato in base al valore del **campo \_ tipo di schema** nella casella tipo di schema (' SCHM ') nell'intestazione MP4 (' Moov ' o ' Moof ').</span><span class="sxs-lookup"><span data-stu-id="2b4bc-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="2b4bc-110">Se il **campo \_ tipo di schema** in un file basato su MP4, o flusso, è impostato su "Cenc" o "cbc1", l' **attributo \_ MFSampleExtension \_ Encryption ProtectionScheme** deve essere impostato su **schema di protezione \_ \_ AES \_ CTR** o **schema di protezione \_ \_ CBC**, rispettivamente e nessun valore deve essere impostato per MFSampleExtension [ \_ Encryption \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock [e \_ MFSampleExtension \_ Encryption](mfsampleextension-encryption-skipbyteblock.md)SkipByteBlock.</span><span class="sxs-lookup"><span data-stu-id="2b4bc-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="2b4bc-111">Se il **campo \_ tipo di schema** in un file basato su MP4, o flusso, è impostato su "cens" o "CBCS", l' **attributo \_ MFSampleExtension \_ Encryption ProtectionScheme** deve essere impostato su **schema di protezione \_ \_ AES \_ CTR** o **schema di protezione \_ \_ CBC**, rispettivamente e MFSampleExtension [ \_ Encryption \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock [e \_ MFSampleExtension \_ Encryption](mfsampleextension-encryption-skipbyteblock.md) SkipByteBlock devono essere impostati usando i valori nella casella "Tenc".</span><span class="sxs-lookup"><span data-stu-id="2b4bc-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="2b4bc-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="2b4bc-112">Examples</span></span>

<span data-ttu-id="2b4bc-113">Nell'esempio seguente viene illustrato come impostare gli attributi **MFSampleExtension \_ Encryption \_ ProtectionScheme** e **MFSampleExtension Encryption \_ \_ CryptByteBlock** e **MFSampleExtension \_ Encryption \_ SkipByteBlock** .</span><span class="sxs-lookup"><span data-stu-id="2b4bc-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="2b4bc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b4bc-114">Requirements</span></span>



| <span data-ttu-id="2b4bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b4bc-115">Requirement</span></span> | <span data-ttu-id="2b4bc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2b4bc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4bc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b4bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b4bc-118">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b4bc-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b4bc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b4bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b4bc-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2b4bc-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="2b4bc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b4bc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b4bc-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b4bc-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
