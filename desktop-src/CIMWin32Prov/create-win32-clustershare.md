---
description: Crea una nuova istanza di \_ ClusterShare Win32.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: edaafa00f792cf01b4166d525171cf15b7f781c8c0c943c17377b3bd9b3401dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020589"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Metodo Create della classe ClusterShare Win32 \_

Crea una nuova [**istanza di \_ ClusterShare Win32.**](win32-clustershare.md)

## <a name="syntax"></a>Sintassi


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* \[ Pollici\]
</dt> <dd>

Percorso locale della condivisione Windows locale.

Ad esempio, "C: \\ Programmi".

</dd> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Alias di un percorso configurato come condivisione in un computer che esegue Windows.

Ad esempio, "public".

</dd> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Tipo di risorsa condivisa. I tipi includono: unità disco, code di stampa, comunicazioni interprocesso (IPC) e dispositivi generali.

<dt>

0 (0x0)
</dt> <dd>

Unità disco

</dd> <dt>

1 (0x1)
</dt> <dd>

Coda di stampa

</dd> <dt>

2 (0x2)
</dt> <dd>

Dispositivo

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Amministratore unità disco

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Amministratore coda di stampa

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Amministratore del dispositivo

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

Amministratore IPC

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, facoltativo\]
</dt> <dd>

Limite al numero massimo di utenti autorizzati a usare questa risorsa contemporaneamente.

</dd> <dt>

*Descrizione* \[ in, facoltativo\]
</dt> <dd>

Descrizione dell'oggetto.

</dd> <dt>

*Password* \[ in, facoltativo\]
</dt> <dd>

DA DEFINIRE

</dd> <dt>

*Accesso* \[ in, facoltativo\]
</dt> <dd>

Istanza incorporata facoltativa di [**una classe \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) che contiene il descrittore di sicurezza per la nuova condivisione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Condivisione cluster \_ Win32**](win32-clustershare.md)
</dt> </dl>

 

