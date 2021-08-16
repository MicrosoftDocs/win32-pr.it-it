---
description: Enumera gli attributi dei file membro nella sezione CatalogFiles di un file di definizione del catalogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Funzione CryptCATCDFEnumAttributesWithCDFTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: f1bffd01865b524b0f06003a6a46b8f81542d7f6113f98db55202e08d8dd7ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768896"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>Funzione CryptCATCDFEnumAttributesWithCDFTag

\[La **funzione CryptCATCDFEnumAttributesWithCDFTag** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La **funzione CryptCATCDFEnumAttributesWithCDFTag** enumera gli attributi dei file membro nella sezione **CatalogFiles** di un file di definizione del catalogo (CDF). **CryptCATCDFEnumAttributesWithCDFTag** viene chiamato da [MakeCat](makecat.md).

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCDF* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CRYPTCATCDF.**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)

</dd> <dt>

*pwszMemberTag* \[ Pollici\]
</dt> <dd>

Puntatore a una **stringa con** terminazione Null che identifica il membro del file di catalogo.

</dd> <dt>

*pMember* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) che contiene le informazioni sui membri.

</dd> <dt>

*pPrevAttr* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) per un attributo del membro file nella funzione CDF a cui punta *pCDF*.

</dd> <dt>

*pfnParseError* \[ Pollici\]
</dt> <dd>

Puntatore a una funzione definita dall'utente per gestire gli errori di analisi dei file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, questa funzione restituisce un puntatore a una [**struttura CRYPTCATATTRIBUTE.**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) La **funzione CryptCATCDFEnumAttributesWithCDFTag** restituisce un **puntatore NULL** in caso di errore.

## <a name="remarks"></a>Commenti

Questa funzione viene in genere chiamata in un ciclo per enumerare tutti gli attributi dei membri del file di catalogo in una funzione definita dall'utente. Prima di immettere il ciclo, *impostare pPrevAttr* su **NULL.** La funzione restituisce un puntatore al primo attributo. Impostare *pPrevAttr* sul valore restituito della funzione per le iterazioni successive del ciclo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la sequenza corretta di assegnazioni per il *parametro pPrevAttr* ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
