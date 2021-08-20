---
title: WINBIO_BIR struttura (Winbio \_ types.h)
description: Rappresenta un record di informazioni biometriche (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR struttura Windows'API Biometric Framework
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
ms.openlocfilehash: beb9e82a27717b33bcd0e06f5cd5bc23a3c43bc3a67cf70068f1a9eeb31b08bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911094"
---
# <a name="winbio_bir-structure"></a>Struttura BIR WINBIO \_

La **struttura \_ BIR WINBIO** rappresenta un record di informazioni biometriche (BIR). Il record di informazioni contiene blocchi di intestazione, dati e firma.

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

Struttura [**WINBIO \_ BIR \_ DATA**](winbio-bir-data.md) che contiene le dimensioni, in byte e l'offset dell'intestazione BIR. L'intestazione contiene informazioni che descrivono il contenuto del record di informazioni.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

Struttura [**WINBIO \_ BIR \_ DATA**](winbio-bir-data.md) che contiene le dimensioni, in byte e l'offset delle informazioni biometriche elaborate o non elaborate create da Windows Biometric Framework (WBF).

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Struttura [**WINBIO \_ BIR \_ DATA**](winbio-bir-data.md) che contiene le dimensioni, in byte e l'offset delle informazioni biometriche elaborate o non elaborate fornite dai sensori e dal software del fornitore.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Struttura [**WINBIO \_ BIR \_ DATA**](winbio-bir-data.md) facoltativa che contiene le dimensioni, in byte e l'offset del codice MAC (Digital Signature Message Authentication Code) che può essere usato per verificare l'integrità del BIR. Se presente, la firma o mac deve coprire l'intestazione e i blocchi di dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso di offset anziché di puntatori consente una serializzazione semplice del BIR e una traduzione meno complessa tra ambienti a 32 e 64 bit o tra modalità utente e kernel.

BiR è compatibile con Common Biometric Exchange Format Framework (CBEFF) definito da NIST 6529-A.

Se questa struttura contiene un *valore StandardDataBlock,* il parametro *Type* dell'intestazione specificata dal parametro *HeaderBlock* deve essere impostato su **WINBIO \_ ANSI \_ 381 \_ FORMAT \_ TYPE.** Questo è l'unico formato dati standard supportato dalla versione corrente del framework biometrico Windows Biometric Framework.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**DATI DI WINBIO \_ BIR \_**](winbio-bir-data.md)
</dt> <dt>

[**INTESTAZIONE DI WINBIO \_ \_ BIR**](winbio-bir-header.md)
</dt> </dl>

 

 





