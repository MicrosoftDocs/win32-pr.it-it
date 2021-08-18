---
description: Utilizzato da un provider del servizio di crittografia (CSP) per verificare la firma di una DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE puntatore a funzione (Cspdk.h)
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
ms.openlocfilehash: b33e6e627c87840e4adb7615f7e3ca5932a7402a3b3ae7110be51c0847a5f67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006679"
---
# <a name="crypt_verify_image-function-pointer"></a>Puntatore a funzione CRYPT \_ VERIFY \_ IMAGE

La funzione di callback **FuncVerifyImage** viene usata da un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) per verificare la firma di una DLL.

Tutte le DLL ausiliarie in cui un CSP effettua chiamate di funzione devono essere firmate nello stesso modo (e con la stessa chiave) della DLL CSP primaria. Per garantire questa firma, le DLL ausiliarie devono essere caricate dinamicamente usando la [**funzione LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Prima del caricamento della DLL, tuttavia, è necessario verificare la firma della DLL. Il CSP esegue questa verifica chiamando la **funzione FuncVerifyImage,** come illustrato nell'esempio seguente.

## <a name="syntax"></a>Sintassi


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszImage* \[ Pollici\]
</dt> <dd>

Indirizzo di una stringa con terminazione Null contenente il percorso e il nome file della DLL per cui verificare la firma.

</dd> <dt>

*pbSigData* \[ Pollici\]
</dt> <dd>

Indirizzo di un buffer che contiene la firma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la funzione ha esito positivo, **FALSE** se ha esito negativo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come usare la funzione di callback **FuncVerifyImage** per verificare la firma di una DLL prima che venga caricata da un CSP.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
