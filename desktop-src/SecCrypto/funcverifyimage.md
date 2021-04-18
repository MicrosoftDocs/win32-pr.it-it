---
description: Utilizzato da un provider del servizio di crittografia (CSP) per verificare la firma di una DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: Puntatore a funzione CRYPT_VERIFY_IMAGE (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312808"
---
# <a name="crypt_verify_image-function-pointer"></a>\_Puntatore alla \_ funzione di verifica immagine Crypt

La funzione di callback **FuncVerifyImage** viene utilizzata da un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per verificare la firma di una dll.

Tutte le DLL ausiliarie in cui un CSP effettua chiamate di funzione devono essere firmate nello stesso modo (e con la stessa chiave) della DLL CSP primaria. Per garantire la firma, le DLL ausiliarie devono essere caricate in modo dinamico tramite la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Ma prima del caricamento della DLL, è necessario verificare la firma della DLL. Il CSP esegue questa verifica chiamando la funzione **FuncVerifyImage** , come illustrato nell'esempio riportato di seguito.

## <a name="syntax"></a>Sintassi


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszImage* \[ in\]
</dt> <dd>

Indirizzo di una stringa con terminazione null che contiene il percorso e il nome file della DLL per cui verificare la firma.

</dd> <dt>

*pbSigData* \[ in\]
</dt> <dd>

Indirizzo di un buffer contenente la firma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la funzione ha esito positivo, **false** in caso di esito negativo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare la funzione di callback **FuncVerifyImage** per verificare la firma di una dll prima che venga caricata da un CSP.


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
