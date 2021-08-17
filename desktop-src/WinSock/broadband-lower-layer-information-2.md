---
description: Questa sezione elenca la definizione del tipo per le informazioni di livello inferiore della banda larga.
ms.assetid: b987dd6b-a611-4297-abaa-fd080cc94f6f
title: Informazioni sul livello inferiore della banda larga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbad3cb209ab8f04417b0bbb89192ed63476b78fd72e3e2a955f72af51b2152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741561"
---
# <a name="broadband-lower-layer-information"></a>Informazioni sul livello inferiore della banda larga

Questa sezione elenca la definizione del tipo per le informazioni di livello inferiore della banda larga.

``` syntax
#include <windows.h>

/* 
 *  values used for the Layer2Mode field in struct ATM_BLLI_IE
 */
#define BLLI_L2_MODE_NORMAL         0x40
#define BLLI_L2_MODE_EXT            0x80

/* 
 *  values used for the Layer3Mode field in struct ATM_BLLI_IE
 */
#define BLLI_L3_MODE_NORMAL         0x40
#define BLLI_L3_MODE_EXT            0x80

/* 
 *  values used for the Layer3DefaultPacketSize field in struct ATM_BLLI_IE
 */
#define BLLI_L3_PACKET_16           0x04
#define BLLI_L3_PACKET_32           0x05
#define BLLI_L3_PACKET_64           0x06
#define BLLI_L3_PACKET_128          0x07
#define BLLI_L3_PACKET_256          0x08
#define BLLI_L3_PACKET_512          0x09
#define BLLI_L3_PACKET_1024         0x0A
#define BLLI_L3_PACKET_2048         0x0B
#define BLLI_L3_PACKET_4096         0x0C



typedef struct {
    DWORD Layer2Protocol;                 /* User information layer 2 protocol           */
    UCHAR Layer2Mode;
    UCHAR Layer2WindowSize;
    DWORD Layer2UserSpecifiedProtocol;    /* User specified layer 2 protocol information */
    DWORD Layer3Protocol;                 /* User information layer 3 protocol           */
    UCHAR Layer3Mode;
    UCHAR Layer3DefaultPacketSize;
    UCHAR Layer3PacketWindowSize;
    DWORD Layer3UserSpecifiedProtocol;    /* User specified layer 3 protocol information */
    DWORD Layer3IPI;                      /* ISO/IEC TR 9577 Initial Protocol Identifier */
    UCHAR SnapID[5];                      /* SNAP ID consisting of OUI and PID           */
} ATM_BLLI_IE;
```

 

 



