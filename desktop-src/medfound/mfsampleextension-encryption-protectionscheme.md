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
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>\_Attributo ProtectionScheme di crittografia MFSampleExtension \_

Specifica lo schema di protezione per gli esempi crittografati.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) . Nei casi in cui l'origine multimediale è basata su MP4, il valore viene impostato in base al valore del **campo \_ tipo di schema** nella casella tipo di schema (' SCHM ') nell'intestazione MP4 (' Moov ' o ' Moof ').

Se il **campo \_ tipo di schema** in un file basato su MP4, o flusso, è impostato su "Cenc" o "cbc1", l' **attributo \_ MFSampleExtension \_ Encryption ProtectionScheme** deve essere impostato su **schema di protezione \_ \_ AES \_ CTR** o **schema di protezione \_ \_ CBC**, rispettivamente e nessun valore deve essere impostato per MFSampleExtension [ \_ Encryption \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock [e \_ MFSampleExtension \_ Encryption](mfsampleextension-encryption-skipbyteblock.md)SkipByteBlock.

Se il **campo \_ tipo di schema** in un file basato su MP4, o flusso, è impostato su "cens" o "CBCS", l' **attributo \_ MFSampleExtension \_ Encryption ProtectionScheme** deve essere impostato su **schema di protezione \_ \_ AES \_ CTR** o **schema di protezione \_ \_ CBC**, rispettivamente e MFSampleExtension [ \_ Encryption \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock [e \_ MFSampleExtension \_ Encryption](mfsampleextension-encryption-skipbyteblock.md) SkipByteBlock devono essere impostati usando i valori nella casella "Tenc".

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare gli attributi **MFSampleExtension \_ Encryption \_ ProtectionScheme** e **MFSampleExtension Encryption \_ \_ CryptByteBlock** e **MFSampleExtension \_ Encryption \_ SkipByteBlock** .


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
