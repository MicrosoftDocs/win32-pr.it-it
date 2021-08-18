---
description: Il metodo Encapsulate incapsula l'UNITÀ APDU (Application Protocol Data Unit) del comando specificato in un altro comando APDU per la trasmissione a un smart card.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: Metodo ISCardCmd::Encapsulate (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f531d0d5f55bea1fe63875a9feb508eb8b4c0e830705bfad2603cc52664c6f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015121"
---
# <a name="iscardcmdencapsulate-method"></a>Metodo ISCardCmd::Encapsulate

\[Il **metodo Encapsulate** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Encapsulate** incapsula l'UNITÀ APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) del comando specificato in un altro comando APDU per la trasmissione a [*un smart card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pApdu* \[ Pollici\]
</dt> <dd>

Puntatore all'APDU da incapsulare.

</dd> <dt>

*ApduType* \[ Pollici\]
</dt> <dd>

Caso ISO 7816-4 per [*trasmissioni T=0.*](../secgloss/t-gly.md)

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

**CASO ISO \_ \_ 1**
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

**CASO ISO \_ \_ 2**
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

**CASO ISO \_ \_ 3**
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

**CASO ISO \_ \_ 4**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *pApdu.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Per compilare un comando APDU, chiamare [**BuildCmd**](iscardcmd-buildcmd.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd.**](iscardcmd.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra come incapsulare un comando APDU. Nell'esempio si presuppone che pIByteApdu sia un puntatore valido a un'istanza [**dell'interfaccia IByteBuffer.**](ibytebuffer.md)


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BuildCmd**](iscardcmd-buildcmd.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
