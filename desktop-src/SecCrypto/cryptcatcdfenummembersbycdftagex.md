---
description: Enumera i singoli membri di file nella sezione CatalogFiles di un file di definizione del catalogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525734"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>CryptCATCDFEnumMembersByCDFTagEx (funzione)

\[La funzione **CryptCATCDFEnumMembersByCDFTagEx** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La funzione **CryptCATCDFEnumMembersByCDFTagEx** enumera i singoli membri di file nella sezione **CatalogFiles** di un file di definizione del catalogo (CDF). **CryptCATCDFEnumMembersByCDFTagEx** viene chiamato da [MakeCat](makecat.md).

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCDF* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszPrevCDFTag* \[ in uscita\]
</dt> <dd>

Puntatore a una stringa con terminazione **null** che identifica il membro del file di catalogo.

</dd> <dt>

*pfnParseError* \[ in\]
</dt> <dd>

Puntatore a una funzione definita dall'utente per gestire gli errori di analisi del file.

</dd> <dt>

*ppMember* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) che contiene le informazioni sui membri del file.

</dd> <dt>

*fContinueOnError* \[ in\]
</dt> <dd>

Valore che specifica se rimanere in memoria un riferimento all'ultimo membro enumerato.

</dd> <dt>

*pvReserved* \[ in\]
</dt> <dd>

Questo parametro è riservato; non usarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Al termine dell'operazione, questa funzione restituisce un puntatore a una stringa con terminazione **null** che identifica un membro del file nella sezione **CATALOGFILES** di un CDF. Se ha esito negativo, la funzione **CryptCATCDFEnumMembersByCDFTagEx** restituisce un puntatore **null** .

## <a name="remarks"></a>Commenti

Questa funzione viene in genere chiamata in un ciclo per enumerare tutti i membri del file di catalogo in un CDF. Prima di immettere il ciclo, impostare *pwszPrevCDFTag* su **null**. La funzione restituisce un puntatore al primo membro. Impostare *pwszPrevCDFTag* sul valore restituito della funzione per le iterazioni successive del ciclo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la sequenza di assegnazioni corretta per il parametro *pwszPrevCDFTag* ( `pwszMemberTag` ).


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
