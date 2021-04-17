---
description: Costruisce un APDU (Command Application Protocol Data Unit) valido per la trasmissione a una smart card.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'Metodo ISCardCmd:: BuildCmd (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232672"
---
# <a name="iscardcmdbuildcmd-method"></a>Metodo ISCardCmd:: BuildCmd

\[Il metodo **BuildCmd** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **BuildCmd** crea un' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) del comando (APDU) valida per la trasmissione a una [*Smart Card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byClassId* \[ in\]
</dt> <dd>

Identificatore della classe di comando.

</dd> <dt>

*byInsId* \[ in\]
</dt> <dd>

Identificatore dell'istruzione del comando.

</dd> <dt>

*byP1* \[ in\]
</dt> <dd>

Primo parametro del comando.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Secondo parametro del comando.

</dd> <dt>

*pbyData* \[ in\]
</dt> <dd>

Puntatore alla parte di dati del comando.

</dd> <dt>

*p1Le* \[ in\]
</dt> <dd>

Puntatore a un valore LONG integer contenente la lunghezza prevista dei dati restituiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno dei parametri non è valido.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>        |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                      |



 

## <a name="remarks"></a>Commenti

Per incapsulare il comando in un altro comando, chiamare [**incapsulate**](iscardcmd-encapsulate.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come creare un comando APDU. Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) e che pIByteRequest sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) inizializzata con una chiamata precedente al metodo [**IByteBuffer:: Initialize**](ibytebuffer-initialize.md) .


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Incapsulare**](iscardcmd-encapsulate.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
