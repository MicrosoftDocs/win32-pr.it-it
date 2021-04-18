---
title: Struttura WINBIO_BIR ( \_ tipi WINBIO. h)
description: Rappresenta un record di informazioni biometriche (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- Struttura di WINBIO_BIR Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302622"
---
# <a name="winbio_bir-structure"></a>\_Struttura WINBIO Bir

La struttura **WINBIO \_ Bir** rappresenta un record di informazioni biometriche (Bir). Il record di informazioni contiene i blocchi di intestazione, dati e firma.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>Members

<dl> <dt>

**HeaderBlock**
</dt> <dd>

Struttura [**di \_ \_ dati WINBIO bir**](winbio-bir-data.md) che contiene le dimensioni, in byte, e l'offset dell'intestazione Bir. L'intestazione contiene informazioni che descrivono il contenuto del record di informazioni.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

Struttura [**di \_ \_ dati WINBIO bir**](winbio-bir-data.md) che contiene le dimensioni, in byte, e l'offset delle informazioni biometriche elaborate o non elaborate create dal Windows Biometric Framework (WBF).

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Una struttura di [**\_ \_ dati WINBIO bir**](winbio-bir-data.md) che contiene le dimensioni, in byte e l'offset delle informazioni biometriche elaborate o non elaborate fornite dai sensori e dal software del fornitore.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Struttura di [**\_ \_ dati WINBIO bir**](winbio-bir-data.md) facoltativa che contiene la dimensione, in byte, e l'offset del codice Mac (Digital Signature Message Authentication Code) che può essere usato per verificare l'integrità di Bir. Se presente, la firma o il MAC deve coprire l'intestazione e i blocchi di dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso degli offset anziché dei puntatori consente una semplice serializzazione di BIR e per una conversione meno complessa tra gli ambienti 32 e 64 bit o tra l'utente e la modalità kernel.

BIR è compatibile con il comune CBEFF (Biometric Exchange Format Framework) definito da NIST 6529-A.

Se questa struttura contiene un valore *StandardDataBlock* , il parametro di *tipo* dell'intestazione specificata dal parametro *HeaderBlock* deve essere impostato sul **\_ \_ \_ \_ tipo di formato WINBIO ANSI 381**. Questo è l'unico formato dati standard supportato dalla versione corrente del Windows Biometric Framework.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**\_dati WINBIO bir \_**](winbio-bir-data.md)
</dt> <dt>

[**\_intestazione WINBIO bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





